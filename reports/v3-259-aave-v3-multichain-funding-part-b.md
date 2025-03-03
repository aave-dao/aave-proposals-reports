# Proposal 259. February Funding Update - Part B

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=259)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-february-funding-update/20712)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x33c0B2efBF3Df1F99187cE93C144b9F725619396)

* Polygon - [proposal payloads](https://polygonscan.com/address/0xfF1FCC6a61910fE28D5Abd94C732a1E1E14f5d6E)

* OP Mainnet - [proposal payloads](https://optimistic.etherscan.io/address/0x677dC488e7F9024673DC0006d6D226585919D85B)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0x89e9e4059af2a8f3D181265BE6916Dd1246A791a)



## Certora Analysis

### Proposal Types

* :moneybag: :receipt: Asset transfers

### Context
This publication presents the February Funding Update - Part B, which consists of performing the following key activities:

Bridging funds to Ethereum;
Create Merit & Ahab Allowances;
Deposit previously swapped assets on Part A

### Proposal Creation
Transaction: [0x92d545d45a52efcae4425097a6b6dd03f93ad9a56f40f0ac7f109a7f9ecfcc5d](https://etherscan.io/tx/0x92d545d45a52efcae4425097a6b6dd03f93ad9a56f40f0ac7f109a7f9ecfcc5d)
- `proposalId`: 259
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x9adc1828386ca02dba7c1a492c4448348addde4551e5bc81968bf49920517b3b

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 252,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 101,
        },
        {
            chain: "10",
            payloads_controller: "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
            payload_id: 68,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 77,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0x9adc1828386ca02dba7c1a492c4448348addde4551e5bc81968bf49920517b3b",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/259.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/252.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/101.md)

* OP Mainnet - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/68.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/77.md)


### Technical Analysis
We have verified that all of the assets have been withdrawn bridged and transferred correctly. Some of the assets were specified to be fully withdrawn but upon contacting with Token Logic the conclusion is that we should leave some dust from each asset.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.