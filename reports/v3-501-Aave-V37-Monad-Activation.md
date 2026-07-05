# Proposal 501. Aave V3.7 Monad Activation

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=501)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-deploy-aave-protocol-on-monad/24943)


## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context

Proposal 501 activates the new **Aave V3.7 market on Monad** (chainId 143) and lists its initial assets, executing the deployment approved through the governance track (TEMP CHECK → Snapshot → ARFC → AIP). Authored by Aave Labs with risk parameters recommended by the DAO's Risk Service Providers (LlamaRisk; forum thread led by TokenLogic) — see the [governance forum](https://governance.aave.com/t/arfc-deploy-aave-protocol-on-monad/24943) and [Snapshot](https://snapshot.org/#/s:aavedao.eth/proposal/0x24f105bd023c476a9b85fa87ff795bfeec769fa799ce6ada8e2724c9738049f6).

The proposal executes **two delegatecall payloads** on the Monad PayloadsController (`0x442CA936e5E6Db875357d0A16481145c96dd9a82`):
- **Payload 1 — Activation:** lists 11 assets (USDT0, USDC, USDe, mUSD, AUSD, WETH, cbBTC, wstETH, weETH, syrupUSDC, sUSDe), creates 4 eMode categories (two stablecoin, two ETH-LST), seeds a first deposit for each reserve into the `DUST_BIN`, and grants the Risk Admin role to the Aave Risk Steward.
- **Payload 2 — GHO listing:** lists GHO (the 12th asset) and adds it as a borrowable to the `syrupUSDC__Stablecoins` and `USDe_sUSDe__Stablecoins` eModes. It **must run after Payload 1**.

Pool admin is intentionally **retained on the Aave Guardian** for the bootstrap period (no admin transfer occurs). The broader GHO cross-chain infrastructure (CCIP lanes, GSM, facilitator minting) discussed on the forum is handled by a **separate proposal** and is **not** in scope here — GHO is listed as an ordinary bridged reserve.

### Proposal Creation
Transaction: [0xfed8753264272a81c277a39f9637b1aa5d5efe1ec81d33ec276a114b26881e71](https://etherscan.io/tx/0xfed8753264272a81c277a39f9637b1aa5d5efe1ec81d33ec276a114b26881e71)
- `proposalId`: 501
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0x698d681b5683c55eb6f7c7c4c8cceafb23d86073c27e1c45cbdf7c7e782cf34f

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "143",
            payloads_controller: "0x442CA936e5E6Db875357d0A16481145c96dd9a82",
            payload_id: 1,
        },
        {
            chain: "143",
            payloads_controller: "0x442CA936e5E6Db875357d0A16481145c96dd9a82",
            payload_id: 2,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x698d681b5683c55eb6f7c7c4c8cceafb23d86073c27e1c45cbdf7c7e782cf34f",
    access_level: 1,
}
```

### Technical Analysis

Both payloads inherit 👻 `AaveV3PayloadMonad` and drive all listings/eModes through the V3 Config Engine. Imports are from `aave-address-book`, `aave-helpers`, `aave-v3-origin` and OpenZeppelin; all globals are `constant`; address-book references (`POOL`, `ORACLE` 👻, `ACL_MANAGER` 👻, `EMISSION_MANAGER`, `DUST_BIN` `0xf23C65…`) resolve in `AaveV3Monad.sol`.

**Listings (12 assets).** Every LTV/LT/LB, cap, reserve factor, rate strategy and oracle value in `newListings()` (and Payload 2's GHO listing) matches the `AaveV3MonadActivation.md` spec tables and `config.ts` decimals to the basis point. Highlights: USDT0/USDC at 75/78/7.5 RF10 (caps 100M; USDC 75M/50M); GHO at 75/78/7.5 (caps 20M/18M); WETH at 80.5/84/5.5 RF15, supply 40k / borrow 36k, borrowing **DISABLED**; cbBTC at 73/78/7 with a steep 10%/300% curve and borrowCap 1; the correlated/LST and yield-stablecoin assets (USDe, mUSD, AUSD, wstETH, weETH, syrupUSDC, sUSDe) listed with **LTV/LT/LB = 0** so they are collateral only inside eModes, with mUSD/AUSD carrying `liqProtocolFee = 0` and weETH a 45% reserve factor.

**eModes (4 created + 2 updated).** `eModeCategoryCreations()` produces `syrupUSDC__Stablecoins` (90/92/4, non-isolated; collateral syrupUSDC; borrowables USDT0/USDC/mUSD/AUSD), `USDe_sUSDe__Stablecoins` (90/92/4, non-isolated; collaterals USDe+sUSDe; borrowables USDT0/USDC/AUSD), and isolated `wstETH__WETH` (94/96/1) and `weETH__WETH` (93/95/1), each with WETH as the sole borrowable. The deliberate asymmetry (mUSD borrowable only in the syrupUSDC eMode) is reproduced faithfully. Payload 2's `assetsEModeUpdates()` adds GHO as borrowable/non-collateral to both stablecoin eModes via `_findEModeCategoryId(label)`.

**WETH borrow gating.** WETH is `enabledToBorrow: DISABLED` yet is the borrowable in both ETH eModes. This is correct under V3.7: `ValidationLogic.validateBorrow` (:121-131) checks the eMode `borrowableBitmap` for non-zero eModes and only checks the reserve `borrowingEnabled` flag for the default category. WETH is therefore borrowable exclusively inside the LST leverage eModes — confirmed by `test_eMode_wstETH__WETH_supplyAndBorrow` / `test_eMode_weETH__WETH_supplyAndBorrow`, while `test_*BorrowWithoutEModeReverts` confirm LTV-0 assets revert with `LtvValidationFailed` outside their eMode.

**Price feeds.** Each asset is priced through a Chainlink SVR feed (18-dec) normalized by a USD-scaling conversion adapter, wrapped by CAPO stable adapters ($1.04 upward cap) for USDT0/USDC/USDe/AUSD, fixed-$1 feeds for mUSD/GHO, and CAPO correlated adapters (7-day snapshot delay, max-yearly-growth sUSDe 11.17% / wstETH 10.70% / weETH 9.53% / syrupUSDC 8.05%) for the LST/correlated assets. The test suite unwraps each adapter to its underlying SVR feed and asserts the growth caps, stable cap, snapshot delay and feed addresses against the LlamaRisk recommendations. **Note:** USDe and sUSDe are priced off the USDT0/USD feed (no USDe-specific feed).

**Permission + seeding.** `_postExecute()` seeds each reserve via `POOL.supply(asset, seed, DUST_BIN, 0)` with decimals correct per asset (100e6 for 6-dec stables, 100e18 for USDe/sUSDe/GHO, 0.0025e18 for ETH assets, 0.0005e8 for cbBTC), then `ACL_MANAGER.addRiskAdmin(0x98217A06…)` — the exact Risk Steward address in the spec. `_supplyAndConfigureLMAdmin` is always passed `lmAdmin = address(0)`, so no emission admin is configured (no LM program proposed). No pool-admin transfer occurs.

**Dependency handling.** Payload 2's `_preExecute()` requires `getReservesCount() > 0` and resolves eMode IDs by label; `test_revertsIfActivationNotExecuted` confirms it reverts if Payload 1 has not run.

The on-chain code faithfully implements the stated intention.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.