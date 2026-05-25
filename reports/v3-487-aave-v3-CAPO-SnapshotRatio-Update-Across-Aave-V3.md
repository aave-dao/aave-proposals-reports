# Proposal 487. CAPO SnapshotRatio Update Across Aave V3

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=487)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-capo-snapshotratio-update-across-aave-v3/24854)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x305479c3F16Da2C925eE3a4c1d81897e536270e8)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x764C854F1c31AF42d9D2c7237d08B7d5321118B8)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x594257acE9A2bAc68F4d102D3Cb3d30774D7122F)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x8D1806E6d80134de48577Ee26b78A6AaA27C1A45)

* Linea - [proposal payloads](https://lineascan.build/address/0xD1E2eCff830d31cb64c4a4a1dFF2622Bc603F23b)

* Plasma - [proposal payloads](https://plasmascan.to/address/0xf191d797050ec73f957003904caf50816fcd3aac)

* Mantle - [proposal payloads](https://mantlescan.xyz/address/0xbb6AB9507951282918789d22383eD413ADE3Ce4b)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates

### Context
LlamaRisk proposes updating the snapshotRatio to address stale snapshots and the growing drift between the CAPO upper bound and the current ratio across Aave V3. This update addresses the risk stemming from the widening spread, where, in the event of an inflation attack, collateral could become materially overpriced, potentially resulting in undercollateralized positions and bad debt for the protocol.

### Proposal Creation
Transaction: [0x175924e7139876b25882ed66c9befdecbfe61e3da433cc76f3654512fc7a3eaf](https://etherscan.io/tx/0x175924e7139876b25882ed66c9befdecbfe61e3da433cc76f3654512fc7a3eaf)
- `proposalId`: 487
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0x755b55250cc12f0983a9261f7f18e520d7c25014e27e1fc5e239096d0821231f

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 441,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 144,
        },
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 115,
        },
        {
            chain: "100",
            payloads_controller: "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
            payload_id: 76,
        },
        {
            chain: "59144",
            payloads_controller: "0x3BcE23a1363728091bc57A58a226CF2940C2e074",
            payload_id: 28,
        },
        {
            chain: "9745",
            payloads_controller: "0xe76EB348E65eF163d85ce282125FF5a7F5712A1d",
            payload_id: 27,
        },
        {
            chain: "5000",
            payloads_controller: "0xF089f77173A3009A98c45f49D547BF714A7B1e01",
            payload_id: 6,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x755b55250cc12f0983a9261f7f18e520d7c25014e27e1fc5e239096d0821231f",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/487.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/441.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/144.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/115.md)

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/76.md)

* Linea - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/59144/0x3BcE23a1363728091bc57A58a226CF2940C2e074/28.md)

* Plasma - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/27.md)

* Mantle - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/5000/0xF089f77173A3009A98c45f49D547BF714A7B1e01/6.md)


### Technical Analysis

* We have verified that the proposal refreshes the CAPO `snapshotRatio` and `snapshotTimestamp` on **19 distinct price-cap adapters across 7 chains**, each adapter resolved to `AaveV3<Chain>.ASSETS.<asset>.ORACLE` in the address book and marked `:ghost:` (recognized) in the per-chain seatbelt. Per-chain breakdown: Ethereum 7 (sUSDe, rETH, weETH, ETHx, osETH, ezETH, cbETH — Core + Prime share the sUSDe and ezETH oracles); Polygon 2 (wstETH, MaticX); Avalanche 2 (sUSDe, sAVAX); Gnosis 2 (wstETH, sDAI); Linea 3 (wstETH, ezETH, weETH); Plasma 2 (sUSDe, weETH); Mantle 1 (sUSDe).
* We have verified that every `(newSnapshotRatio, newSnapshotTimestamp)` pair in the seatbelt state-diff exactly matches the IPFS specification table (e.g. osETH `1014445878439441413 → 1069243791626177773`, sUSDe `1150485992969698694 → 1227131992751411096`, sAVAX `1130535654847205789 → 1258004893989529449`). All new timestamps fall in the range `1776040248 – 1776100271` (April 13, 2026).
* We have verified the additional `maxYearlyRatioGrowthPercent` tightening on the sUSDe Ethereum adapter (`0x42bc86f2f08419280a99d8fbEa4672e7c30a86ec`, shared by Core + Prime): `5000 → 1117` bps (50.00% → 11.17%), matching the spec's explicit recommendation. No other adapter changes `maxYearlyRatioGrowthPercent`.
* We have verified that every adapter's new `maxRatioGrowthPerSecond` equals `(newSnapshotRatio × maxYearlyRatioGrowthPercent_bps) / (31,536,000 × 10,000)` exactly — i.e. the seatbelt-visible change to this field is the automatic recomputation inside `_setCapParameters` after a snapshot update, not a separate parameter retune. Mantle uses the `Scaled` variant of this field per its adapter precision convention.
* We have verified that the direct-to-AIP safety boundary is enforced on-chain: `_setCapParameters` requires `newTimestamp > stored`, `MINIMUM_SNAPSHOT_DELAY ≤ age`
* We have verified that no other state changes occur.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.