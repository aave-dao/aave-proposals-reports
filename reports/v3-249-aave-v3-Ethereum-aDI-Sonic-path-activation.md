# Proposal 249. a.DI Sonic path activation

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=249)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/technical-maintenance-proposals/15274/69)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x41FE455778201FB3AC7E41a7b2B4ffC90F08035e)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking

### Context
Proposal to register the necessary Sonic adapters on a.DI, a technical pre-requirement for an activation vote of Aave v3 Sonic.

### Proposal Creation
Transaction: [0x7f88fea9abb98ceed5199091e24aeebf7c9acf3a01287c0ef8e36a00f37ff48b](https://etherscan.io/tx/0x7f88fea9abb98ceed5199091e24aeebf7c9acf3a01287c0ef8e36a00f37ff48b)
- `proposalId`: 249
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0xf0b7b7dd28d63e71f7b4f65a4eeb0058d06ac5911098554fc1d2dbe507d64f78

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 246,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0xf0b7b7dd28d63e71f7b4f65a4eeb0058d06ac5911098554fc1d2dbe507d64f78",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/249.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/246.md)


### Technical Analysis
We verified that the payload is adding the declared bridge adapters on Ethereum for the Sonic network in the correct role - forwarder as described in the IPFS.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.