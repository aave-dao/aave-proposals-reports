# Proposal 294. Mantle a.DI path activation

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=294)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/technical-maintenance-proposals/15274/81)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x184CA99Cd89313c00a69b9A8E1649D84FBD8D86D)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking



### Context
Proposal to activate the necessary a.DI and governance infrastructure for the Mantle network, a technical prerequisite for an activation vote of Aave v3 Mantle.

### Proposal Creation
Transaction: [0x6ef35d2fe7f159681b2a4d3d21e780c36278a1f2b53a0f9ce9a364241f210962](https://etherscan.io/tx/0x6ef35d2fe7f159681b2a4d3d21e780c36278a1f2b53a0f9ce9a364241f210962)
- `proposalId`: 294
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x843f8e79d8b8a8d16f67b3b612386459ec256ed0118f0452c9f8f75b39c929c0

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 271,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x843f8e79d8b8a8d16f67b3b612386459ec256ed0118f0452c9f8f75b39c929c0",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/294.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/271.md)


### Technical Analysis

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.