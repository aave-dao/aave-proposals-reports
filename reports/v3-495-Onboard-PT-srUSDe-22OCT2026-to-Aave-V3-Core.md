# Proposal 495. Onboard PT-srUSDe-22OCT2026 to Aave V3 Core

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=495)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-onboard-strata-srusde-22oct2026-pt-tokens-to-v3-core-instance/25113)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xBE8B76b55734F277156eC5702408bF210a6fC23b)

## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context

Proposal 495, authored by **Aave Labs** under the DAO-approved **direct-to-AIP** process, onboards **PT-srUSDe-22OCT2026** ([`0x59bC9FaE5D62B19d4f8d07D758047aCb9EE19d34`](https://etherscan.io/address/0x59bC9FaE5D62B19d4f8d07D758047aCb9EE19d34)) — Pendle's Principal Token for Strata's srUSDe maturing 22 Oct 2026 — to the **Aave V3 Core** instance on Ethereum. It is positioned as a natural rollover destination ahead of the expiry of PT-srUSDe-25JUN2026. The PT is listed borrow-disabled with zero base LTV/LT and is made usable as collateral exclusively through two newly created **isolated e-mode categories** (`PT-srUSDe Stablecoins` and `PT-srUSDe USDe`) that pair it with sUSDe against stablecoin borrowing. Pricing uses a dynamic **linear discount-rate oracle** (`0xBD1bc41479D0b58167584980fE57fDA913d4fB73`) over a capped USDT/USD Chainlink feed (initialDiscountRatePerYear 5.31%, maxDiscountRatePerYear 10.22%). See the [forum discussion](https://governance.aave.com/t/direct-to-aip-onboard-strata-srusde-22oct2026-pt-tokens-to-v3-core-instance/25113).

### Proposal Creation
Transaction: [0x16cca074023e33856ca2362df7a7ccf6e9a68c728fd7b34180da07e7ef5e5777](https://etherscan.io/tx/0x16cca074023e33856ca2362df7a7ccf6e9a68c728fd7b34180da07e7ef5e5777)
- `proposalId`: 495
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0x8c0576af9e4f45178d42ddbd81293ecc5ed0aa1f738b9c0382594a65049af0c9

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 448,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x8c0576af9e4f45178d42ddbd81293ecc5ed0aa1f738b9c0382594a65049af0c9",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/495.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/448.md)


### Technical Analysis
## Technical Analysis

The payload `AaveV3Ethereum_OnBoardPTsrUSDe22Oct2026EthereumCore_20260617` inherits `AaveV3PayloadEthereum` and drives the change entirely through the **config engine** — no direct `poolConfigurator` calls. All globals are `constant`; imports are from `aave-address-book`, `aave-helpers`, and `aave-v3-origin` (👻-recognized sources). Execution is a single `delegatecall` by the PayloadsController.

**Listing (`newListings()`):**

| Parameter | Payload | Spec | Match |
|---|---|---|---|
| asset | `0x59bC9…19d34` (PT proxy, 18 dec) | same | ✅ |
| priceFeed | `0xBD1bc…4fB73` (8 dec, ans ≈ $0.9808) | `0xbd1bc…4fb73` | ✅ |
| enabledToBorrow | DISABLED | DISABLED | ✅ |
| flashloanable | DISABLED | DISABLED | ✅ |
| ltv / liqThreshold / liqBonus | 0 / 0 / 0 | 0 / 0 / 0 | ✅ |
| reserveFactor | 45_00 | 45% | ✅ |
| supplyCap | 25,000,000 | 25,000,000 | ✅ |
| borrowCap | 1 | 1 | ✅ |
| liqProtocolFee | 10_00 | 10% | ✅ |
| rates (Uopt/base/s1/s2) | 45 / 0 / 10 / 300% | 45 / 0 / 10 / 300% | ✅ |

The resulting reserve has id 66; aToken `aEthPT_srUSDe_22OCT2026` and variableDebtToken are initialized against POOL `0x8787…`. Base LTV/LT = 0 means the asset carries no borrowing power outside e-mode (the standard PT pattern); the seatbelt diff confirms the executed reserve (id 66, oracle 8 decimals, `oracleLatestAnswer` 0.98079259).

**E-mode creation (`eModeCategoryCreations()`):** two **isolated** categories, confirmed in the diff —
- **id 47 — PT-srUSDe Stablecoins:** ltv 8842, LT 9042, LB 10568 (5.68%); collateral {sUSDe, PT}; borrowable {USDC, USDT, USDe}.
- **id 48 — PT-srUSDe USDe:** ltv 9106, LT 9306, LB 10268 (2.68%); collateral {sUSDe, PT}; borrowable {USDe}.
Bitmaps decode consistently (PT id 66, sUSDe id 32, USDC id 3, USDT id 8, USDe id 30). Liquidation bonuses are stored as `100_00 + bonus` (10568 / 10268), matching the config-engine convention and the test assertions.

**First-deposit seed:** `_postExecute()` calls `_supplyAndConfigureLMAdmin(PT, 1e18, address(0))`, which `forceApprove`s and supplies 1 PT (1e18) on behalf of `AaveV3Ethereum.DUST_BIN`, mitigating the first-deposit/inflation attack. Because `lmAdmin == address(0)`, the `setEmissionAdmin` branch is dead code and no LM program is configured. The diff shows the Supply event and a DUST_BIN aToken balance of 1e18.

**Tests:** `defaultTest` config snapshot, dust-bin balance assertion (`test_dustBinHasPT_srUSDe_22OCT2026Funds`), full e-mode config assertions (LTV/LT/LB, isolation flags, collateral/borrowable bitmaps), supply→borrow→repay→withdraw round-trips in both e-modes, and a negative test proving borrow reverts without e-mode (`LtvValidationFailed`). 👻 Aave-recognized contracts (POOL `0x8787…`, POOL_CONFIGURATOR, ORACLE `0x5458…`, PAYLOADS_CONTROLLER `0xdAba…`) behave as expected; Seatbelt reports no failed checks.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.

