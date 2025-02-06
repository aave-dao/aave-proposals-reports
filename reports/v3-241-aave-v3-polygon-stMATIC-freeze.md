# Proposal 241. Sunset stMATIC on Polygon instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=241)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-sunset-stmatic-on-polygon-instance/20668)

### Payloads

* Polygon - [proposal payloads](https://polygonscan.com/address/0xC35feff10e26eF64C17076539EbDb156dBae5BFe)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
Given [Lido’s recent announcement to sunset stMATIC](https://blog.lido.fi/lido-on-polygon-sunset/) (their Liquid Staking Token implementation on Polygon), we propose freezing the stMATIC reserve on the Aave V3 Polygon market. This freeze would prevent users from increasing supply or creating new borrow positions, while maintaining functionality for repayments, withdrawals, and liquidations.

### Proposal Creation
Transaction: [0xfa88e0da4001f59c6dbc91408a33b021332a6823e0dd8789f1b348e4f8d6fd2f](https://etherscan.io/tx/0xfa88e0da4001f59c6dbc91408a33b021332a6823e0dd8789f1b348e4f8d6fd2f)
- `proposalId`: 241
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x4fb4b85caf14ac9be96975a2d062f4e728d7fcebd01a70b4d57532c672fb4f4a

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 96,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0x4fb4b85caf14ac9be96975a2d062f4e728d7fcebd01a70b4d57532c672fb4f4a",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/241.md)

**Payload Reports**

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/96.md)


### Technical Analysis
We have verified the freeze has been set to true.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.