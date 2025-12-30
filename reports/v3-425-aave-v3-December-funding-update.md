# Proposal 425. December Funding Update

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=425)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-december-2025-funding-update/23619)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x4C87E8F0Ec0BCd886ab5f4f06Fc5AF56254D5111)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates


### Context

This publication presents the December Funding Update, consisting of the following key activities:

Acquire GHO to support runway;
Expand the remit of the AFC & Ahab SAFEs to support GHO liquidity; and
Create allowances to support operations.

### Proposal Creation
Transaction: [0xa3b7ac2f2ca61492558b533080ee2d351c65bbfb24030a9ba2d0abd4f1c2d8c6](https://etherscan.io/tx/0xa3b7ac2f2ca61492558b533080ee2d351c65bbfb24030a9ba2d0abd4f1c2d8c6)
- `proposalId`: 425
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xe3e08d0a94663b716898f9a6527b8446b6e65dccae338c35742bc4bc6d6f81bd

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 384,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xe3e08d0a94663b716898f9a6527b8446b6e65dccae338c35742bc4bc6d6f81bd",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/425.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/384.md)


### Technical Analysis
We have verified alignment between the forum, IPFS, and the payload. We have checked the integrity of the imports. We have validated all approval amounts with respect to decimal precision and the correct spender addresses. We have validated the deposit of idle `ETH` to the Prime instance.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.