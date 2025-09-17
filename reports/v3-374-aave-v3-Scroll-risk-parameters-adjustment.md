# Proposal 374. Risk Parameter Adjustments for Aave V3 Scroll Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=374)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-risk-parameter-adjustments-for-aave-v3-scroll-instance/23113)

### Payloads

* Scroll - [proposal payloads](https://scrollscan.com/address/0x24A9917056a60E12Cf7FAa824DE059f9a86ffdbF)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
This Direct to AIP proposes immediate risk parameter adjustments for all assets on the Aave V3 Scroll instance to mitigate potential risks arising from ongoing governance instability within the Scroll ecosystem. The proposal seeks to increase Reserve Factors (RF) across all assets.

### Proposal Creation
Transaction: [0x7cd315a0e7bb40fc4b149e695efafaa8fc63ad6037a418d25ed741bba6eb59ff](https://etherscan.io/tx/0x7cd315a0e7bb40fc4b149e695efafaa8fc63ad6037a418d25ed741bba6eb59ff)
- `proposalId`: 374
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x320cbae85b0351f558eef82885ea9b8a17b130c55eaad81064657e00ce48d9c5

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "534352",
            payloads_controller: "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE",
            payload_id: 46,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x320cbae85b0351f558eef82885ea9b8a17b130c55eaad81064657e00ce48d9c5",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/374.md)

**Payload Reports**

* Scroll - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/46.md)


### Technical Analysis
We have verified the correct changes to the reserve factor have been implemented tot he correct assets

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.