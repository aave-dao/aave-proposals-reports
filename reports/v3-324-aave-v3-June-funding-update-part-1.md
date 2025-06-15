# Proposal 324. June Funding Update - Part I

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=324)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-june-2025-funding-update/22352/2)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x25C30d5E07B23C30d0E25da544A9815CA7218C03)



## Certora Analysis

### Proposal Types
* :moneybag: :receipt: Asset transfers
* :handshake: Permission granting and revoking


### Context
This publication presents the Part 1 of the June Funding Update, consisting of the following key activities:

- Continue AAVE buybacks for 2 weeks.

### Proposal Creation
Transaction: [0x19f3eddc8cdea0ed262893370cebc36014353d31d6d29b6a9adee9ad8e2edca6](https://etherscan.io/tx/0x19f3eddc8cdea0ed262893370cebc36014353d31d6d29b6a9adee9ad8e2edca6)
- `proposalId`: 324
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x49ad36f79f5aa2fc047c56cc9015552b9083fdc79cc5ed355d1a16b0296fd1c9

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 299,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x49ad36f79f5aa2fc047c56cc9015552b9083fdc79cc5ed355d1a16b0296fd1c9",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/324.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/299.md)


### Technical Analysis
The precision and the amount are as inteded in the IPFS. The approved address is correct.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.