# Proposal 254. Adjust Risk Parameters for Aave V2 and V3 on Polygon

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=254)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-adjust-risk-parameters-for-aave-v2-and-v3-on-polygon/20211)

### Payloads

* Polygon - [proposal payloads](https://polygonscan.com/address/0x100c6aB6Dc8875Aa6023DA8aD04b352414b47cD3)

* Polygon 2 - [proposal payloads](https://polygonscan.com/address/0xd0391675Ac61Ed550F6e5241535e59544ec94c19)



## Certora Analysis

### Proposal Types
* :wrench: :bar_chart: Configuration updates

### Context
Following Polygon's evaluation on assets bridged using the PoS portal bridge, and after risk assessment by the risk providers, the AIP suggest to adjust parameters for some of the most utilized bridged stables on Polygong.

### Proposal Creation
Transaction: [0xa3e80826228537f1ae288fa78ba45a91d4f20e5cd5665ddd9db859a9c7cb8180](https://etherscan.io/tx/0xa3e80826228537f1ae288fa78ba45a91d4f20e5cd5665ddd9db859a9c7cb8180)
- `proposalId`: 254
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x9a0342bc6f37687ea20210c3a1664de1949d9e3e967ff87467501d4d00116aab

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 100,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0x9a0342bc6f37687ea20210c3a1664de1949d9e3e967ff87467501d4d00116aab",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/254.md)

**Payload Reports**

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/100.md)

* Polygon 2 - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/100.md)


### Technical Analysis
The payload adjust the LTV of the 6 specified assets on Aave V2 and V3 on Polygon to 0,
In addition it was verified that no other parameters were modified except for the 3 reserve factor updates specified in the IPFS.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.