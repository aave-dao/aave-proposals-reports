# Proposal 373. Request for Bounty Payout - August 2025

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=373)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/bgd-request-for-bounty-payout-august-2025/23096)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x00FBA59Da30666F4ED13746D592bbE82307E7914)



## Certora Analysis

### Proposal Types

* :moneybag: :receipt: Asset transfers



### Context
Proposal to release a total of $13’000 as bounty for two outstanding `Aave <> Immunefi` valid submissions, together with $1’300 as the fee to the Immunefi platform; amounting to a grand total of $14'300.

The asset of payment will be `GHO`.

### Proposal Creation
Transaction: [0xd791b305797d2b77ea139b94f0a41516b0c9fe84e498572a41ec5c3625f389b6](https://etherscan.io/tx/0xd791b305797d2b77ea139b94f0a41516b0c9fe84e498572a41ec5c3625f389b6)
- `proposalId`: 373
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x1582c62ea9232ca3ce28c23a8a2a75dc82a8b5962094b9cea8819588acb3b1ad

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 340,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x1582c62ea9232ca3ce28c23a8a2a75dc82a8b5962094b9cea8819588acb3b1ad",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/373.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/340.md)


### Technical Analysis
We have verified the amounts and addresses match the forum and IPFS. 
The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.