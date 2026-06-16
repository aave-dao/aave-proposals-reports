# Proposal 493. Onboard PT-sUSDe-22OCT2026 to Aave v3 Plasma

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=493)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-onboard-pt-susde-22oct2026-to-aave-v3-plasma/25129)

### Payloads

* Plasma - [proposal payloads](https://plasmascan.to/address/0xb0f1747036a9671e1f7c484e7377cded464ea1c4)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets
* :wrench: :bar_chart: Configuration updates

### Context
This proposal seeks to onboard PT-sUSDe-22OCT2026 to the Aave V3 Plasma Instance.

### Proposal Creation
Transaction: [0x86933e3b27e71d88e14e2bc2b773a65927995b63efa2c20b68e6c4e066e16372](https://etherscan.io/tx/0x86933e3b27e71d88e14e2bc2b773a65927995b63efa2c20b68e6c4e066e16372)
- `proposalId`: 493
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0x34ff9f11fe33c0d09b4ed35dc48e17135d2997993e55bb147580c36df9540f05

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "9745",
            payloads_controller: "0xe76EB348E65eF163d85ce282125FF5a7F5712A1d",
            payload_id: 30,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x34ff9f11fe33c0d09b4ed35dc48e17135d2997993e55bb147580c36df9540f05",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/493.md)

**Payload Reports**

* Plasma - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/30.md)


### Technical Analysis

* We have verified that the payload lists `PT-sUSDE-22OCT2026` (`0xf7fB83435F455Bd970F2D9f943f4eECE1941b3e9`, 18 decimals, `PendlePrincipalToken`) as reserve id 17, increasing `_reservesCount` from 17 to 18, matching the token address on the forum and IPFS. The reserve is configured with a `150,000,000` supply cap, a 45% reserve factor, a 10% liquidation protocol fee, virtual accounting enabled, and borrowing and flash-loaning disabled (borrow cap `1`), i.e. collateral-only — matching the forum's "Borrowable: No" specification.
* We have verified that the AaveOracle price source for the asset is set to the `PendlePriceCapAdapter` at `0x9c823f4e19Ef68347810a9C139619273b8282b7e` (`latestAnswer` ≈ `0.9842`, 8 decimals). Reading the adapter on-chain confirms `PENDLE_PRINCIPAL_TOKEN` is the listed PT, `ASSET_TO_USD_AGGREGATOR` is the recognized USDT0 `PriceCapAdapterStable` (`0xdBbB0b5DD13E7AC9C56624834ef193df87b022c3`), `MATURITY` is `1792627200` (22 Oct 2026), and the linear-discount rates are 4.37% initial / 12.27% maximum — consistent with the forum's discount-oracle parameters.
* We have verified that two new isolated e-mode categories are created: category 25 `sUSDe_PT_sUSDe_22OCT2026__Stablecoins` (LTV 87.71% / LT 89.71% / LB 4.87%; collateral `sUSDe`, `PT-sUSDE-22OCT2026`; borrowable `USDT0`, `USDe`, `GHO`) and category 26 `sUSDe_PT_sUSDe_22OCT2026__USDe` (LTV 90.35% / LT 92.35% / LB 1.87%; collateral `sUSDe`, `PT-sUSDE-22OCT2026`; borrowable `USDe`). Both match the forum exactly and satisfy `LT × (1 + LB) ≈ 0.9408 < 1`, so liquidations at threshold do not create bad debt.
* We have verified that the first-deposit-attack mitigation is applied: 1 PT (`1e18`) is supplied on behalf of `DUST_BIN` (`0x300f49ddf6fB9358ddCB22b12fFae62F1Cce9CdD`, recognized in `AaveV3Plasma.sol`), and the new `aPlaPT_sUSDE_22OCT2026` aToken (`0x34D33fCaCC36b9A16CE1Cab8d7FB1CAF8B7C2d00`) and `variableDebtPlaPT_sUSDE_22OCT2026` (`0x8e1D74cf7bdD9F0339f807156F557536dF32a050`) are initialized with treasury set to the Collector (`0x5E2d083417D12d4B0824E14Ecd48D26831F4Da7D`) and the default incentives controller.
* We have verified that no other state changes occur.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.