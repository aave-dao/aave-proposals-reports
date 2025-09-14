# Proposal 372.  Increase rsETH Supply Cap on Aave V3 Linea Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=372)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-increase-rseth-supply-cap-on-aave-v3-linea-instance/23073)

### Payloads

* Linea - [proposal payloads](https://lineascan.build/address/0x393cb9078fe3610D0daFAf3369EE61Fe78dcCB95)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
This proposal seeks to increase the rsETH supply cap on the Aave V3 Linea instance to accommodate growing demand and prevent supply cap limitations that restrict user access.

### Proposal Creation
Transaction: [0x81f871aa7f62905030237ead60fee731caec2a80914845507c3e51172479eb5d](https://etherscan.io/tx/0x81f871aa7f62905030237ead60fee731caec2a80914845507c3e51172479eb5d)
- `proposalId`: 372
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xb3ad06ee2ae1d97b762191b6ca4cabd3271a24a9eb9f8d37d8f1737bbb957f69

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "59144",
            payloads_controller: "0x3BcE23a1363728091bc57A58a226CF2940C2e074",
            payload_id: 13,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xb3ad06ee2ae1d97b762191b6ca4cabd3271a24a9eb9f8d37d8f1737bbb957f69",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/372.md)

**Payload Reports**

* Linea - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/59144/0x3BcE23a1363728091bc57A58a226CF2940C2e074/13.md)


### Technical Analysis
The specified amount on the payload match the amount on the IPFS and forum. The payload successfully increase the supply cap of `rsETH`.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.