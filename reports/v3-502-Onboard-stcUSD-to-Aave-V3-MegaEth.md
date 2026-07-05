# Proposal 502. Onboard stcUSD to Aave V3 MegaEth

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=502)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-onboard-stcusd-to-aave-v3-megaeth/25018)

### Payloads

* MegaETH - [proposal payloads](https://mega.etherscan.io/address/0x72a0b6b3a3cd69e9ca11b70cc06cb5b98b8e9ac5)


## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets

### Context
Proposal 502 onboards **stcUSD** (Staked Cap USD, `0x88887bE419578051FF9F4eb6C858A951921D8888`) to the **Aave V3 MegaETH** deployment as a new reserve. stcUSD is a yield-bearing stablecoin from Cap Protocol — an ERC-4626 vault wrapping cUSD on Ethereum and bridged to MegaETH via LayerZero. The risk assessment is by **LlamaRisk** and the technical implementation by **Aave Labs**. The asset is listed as collateral-only (borrowing and flashloans disabled) with base LTV/LT/LB = 0, becoming usable as collateral exclusively inside a new isolated e-mode `stcUSD__Stablecoins` (LTV 88% / LT 90% / LB 4%) against USDT0 and USDm — enabling stablecoin looping without exposing Aave to direct stcUSD borrow or flashloan risk. References: [forum ARFC](https://governance.aave.com/t/arfc-onboard-stcusd-to-aave-v3-megaeth/25018), Snapshot `0x84ccc14e104b18a74ef47375ccd59f7f7aeeb61716dbb2c362ea7a538da3e08f`.

### Proposal Creation
Transaction: [0x089b3daa50dfe928ddfbd7787dfddbc8c3eebb115de76a86eed0b5fd004b33b8](https://etherscan.io/tx/0x089b3daa50dfe928ddfbd7787dfddbc8c3eebb115de76a86eed0b5fd004b33b8)
- `proposalId`: 502
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0xd3036aa0df8a4a04be7048fee749f6cad838ad0121176659b361b88eb1890258

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "4326",
            payloads_controller: "0x80e11cB895a23C901a990239E5534054C66476B5",
            payload_id: 8,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xd3036aa0df8a4a04be7048fee749f6cad838ad0121176659b361b88eb1890258",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/502.md)

**Payload Reports**

* MegaETH - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/4326/0x80e11cB895a23C901a990239E5534054C66476B5/8.md)


### Technical Analysis
The single MegaETH payload `AaveV3MegaEth_OnboardStcUSDMegaEth_20260624` inherits `AaveV3PayloadMegaEth` and implements the standard config-engine entry points.

**Listing (`newListings`)** — asset `stcUSD` = `0x88887bE419578051FF9F4eb6C858A951921D8888` (proxy on MegaETH), priced by adapter `0xBBC579Ee0A3fD6E9240965C5f57b7e5b3e3809A8`:
- `enabledToBorrow` / `flashloanable`: DISABLED
- `ltv` / `liqThreshold` / `liqBonus`: 0 / 0 / 0 (collateral usability deferred to the e-mode)
- `supplyCap`: 10,000,000 · `borrowCap`: 1 (inert, borrowing disabled) · `liqProtocolFee`: 10.00% · `reserveFactor`: KEEP_CURRENT
- rate strategy: optimal usage 45.00%, base 0, slope1 10.00%, slope2 300.00%
All match the forum table (borrow cap is N/A in spec; on-chain `1` is cosmetic since borrowing is off).

**E-mode (`eModeCategoryCreations`)** — creates category 8 `stcUSD__Stablecoins`: LTV 88.00%, LT 90.00%, LB 4.00% (engine stores 104_00), `isolated: true`, collaterals = [stcUSD], borrowables = [`USDT0_UNDERLYING` `0xB8CE…ebb`, `USDm_UNDERLYING` `0xFAfD…79E7`]. Both borrowable addresses match the address-book (`AaveV3MegaEth.sol:130,151`) and the seatbelt report.

**Oracle** — the adapter is a CAPO price-cap adapter `Capped stcUSD / USDC / USD`: `RATIO_PROVIDER` = `STCAPUSD / CAPUSD Exchange Rate` (stcUSD/cUSD) × `BASE_TO_USD_AGGREGATOR` = `Capped USDC/USD` (`0x9182ACce…FE07`), 8 decimals, 14-day min snapshot delay, 10.50% max yearly growth, asserted price within [0.98, 1.15]. ⚠️ Note: the forum described the second leg as **cUSD/USD**; the implementation proxies cUSD with a **capped USDC/USD** feed (see Intention / Logical review). The adapter is a brand-new contract, absent from the address-book and unidentified by provider checks; it has no code at its embedded snapshot block, so the snapshot is anchored indirectly via the underlying ratio feed (`test_stcUSDCapoSnapshotAnchored`).

**First deposit (`_postExecute`)** — `_supplyAndConfigureLMAdmin(stcUSD, 1e18, address(0))` force-approves the POOL and supplies 1 coin (1e18) on behalf of the `DUST_BIN` (`AaveV3MegaEth.DUST_BIN`), preventing the empty-reserve / first-deposit-inflation attack. `lmAdmin == address(0)`, so the emission-admin branch is skipped (intentional). The seed is supplied from the **executor's own delegatecall-context balance** — the test deals stcUSD to `EXECUTOR_LVL_1` because the executor must be pre-funded on-chain before execution.

**Tests** — `defaultTest` plus dedicated checks: `test_stcUSDPriceFeedMatchesLlamaRiskConfig` (14-day snapshot delay, 10.50% max yearly growth, 8 decimals, USDC/USD base + stcUSD/cUSD ratio), `test_stcUSDOraclePriceReflectsCapo`, `test_stcUSDCapoSnapshotAnchored`, `test_dustBinHasstcUSDFunds`, `test_eModeConfiguration`, `test_eMode_StcUSD__Stablecoins_supplyAndBorrow`, and `test_stcUSDBorrowWithoutEModeReverts` (non-e-mode borrow reverts with `LtvValidationFailed`).


The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.