# Proposal 470. Deprecate Aave V3 Scroll Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=470)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-aave-v3-scroll-instance-deprecation/24432)

### Payloads

* Scroll - [proposal payloads](https://scrollscan.com/address/0xD233c9a667dd8535C51f174F9535553A4db72e97)



## Certora Analysis

### Proposal Types


* :wrench: :bar_chart: Configuration updates


### Context
Following the Risk Stewards cap reduction executed on April 10, 2026, this proposal completes the deprecation of Aave V3 on Scroll by freezing all assets and increasing the reserve factor on select assets.

### Proposal Creation
Transaction: [0x281587c5159c5eefc360ae7f07179a67dad5754823a1bdc40607becedefb3fb5](https://etherscan.io/tx/0x281587c5159c5eefc360ae7f07179a67dad5754823a1bdc40607becedefb3fb5)
- `proposalId`: 470
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0x1434716f99a33c43c3531821ef6e648e144768a1ae0c133fbcbe954e7934f614

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "534352",
            payloads_controller: "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE",
            payload_id: 51,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x1434716f99a33c43c3531821ef6e648e144768a1ae0c133fbcbe954e7934f614",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/470.md)

**Payload Reports**

* Scroll - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/51.md)


### Technical Analysis

We have verified the successful freezing of the following assets: WETH, USDC, wstETH, weETH, and SCR.

We have validated the reserve factor increase from 50% to 85% for all specified assets, excluding WETH, which correctly remains unchanged.

We have verified the payload's logic and validated its execution via Seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.