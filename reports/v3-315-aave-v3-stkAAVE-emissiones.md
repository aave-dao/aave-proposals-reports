# Proposal 315. stkAAVE Emissions

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=315)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-amend-safety-module-emissions/16640/26)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x3BA3AA11d335371b143E7E6BE9Eeaa4A42CCF26B)



## Certora Analysis

### Proposal Types

* :moneybag: :receipt: Asset transfers
* :handshake: Permission granting and revoking


### Context
Re-enable stkAAVE incentives emissions for 90 days in anticipation of the launch of Umbrella.

### Proposal Creation
Transaction: [0x8fb0ad35806a95650f58b4fcb4db67e62f7c3ca0ad1cff87a99c61a203e8f3c8](https://etherscan.io/tx/0x8fb0ad35806a95650f58b4fcb4db67e62f7c3ca0ad1cff87a99c61a203e8f3c8)
- `proposalId`: 315
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xa48e4cf9a666d6a86f7e336fcfd8b88a187686053ab1b7eeba2bc5283629af8f

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 291,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xa48e4cf9a666d6a86f7e336fcfd8b88a187686053ab1b7eeba2bc5283629af8f",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/315.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/291.md)


### Technical Analysis
We have verified the new allowance suit the amount specified in the ipfs and forum.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.