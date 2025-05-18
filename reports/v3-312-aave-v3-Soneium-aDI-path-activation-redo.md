# Proposal 312. Soneium aDI path activation

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=312)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/technical-maintenance-proposals/15274/83)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xD934A9034C95f9c31e1D6077DFed49B0F4d36FC3)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking


### Context
Proposal to register the necessary Soneium adapters on a.DI, a technical pre-requirement for an activation vote of Aave v3 Soneium.

### Proposal Creation
Transaction: [0x21f583e08fd698c1727b4874f3fef705656cefa33a3647c0b3e2b97e35b961ec](https://etherscan.io/tx/0x21f583e08fd698c1727b4874f3fef705656cefa33a3647c0b3e2b97e35b961ec)
- `proposalId`: 312
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0xde635f0d662264f561dbd690f3a80a4b52d03c80758cba4dc9c958316422e325

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 287,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xde635f0d662264f561dbd690f3a80a4b52d03c80758cba4dc9c958316422e325",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/312.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/287.md)


### Technical Analysis
We have validated the specified addresses and confirmed the 1 out of 1 path.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.