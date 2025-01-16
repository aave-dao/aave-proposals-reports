it # Proposal 232. a.DI Celo path activation

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=232)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/technical-maintenance-proposals/15274/61)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x8F7E2023686B78E148e65004Ca8AcEf9B2B46922)



## Certora Analysis

### Proposal Types
* :handshake: Permission granting and revoking

### Context
In order to enable DAO control over a Celo instance of Aave, the aDI needs to be activated and  configured to allow it.

### Proposal Creation
Transaction: [0xb61b67521e48601acce8b9f95e823b801557183e1d514d0839b9db7fcbad59af](https://etherscan.io/tx/0xb61b67521e48601acce8b9f95e823b801557183e1d514d0839b9db7fcbad59af)
- `proposalId`: 232
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0xbc14f660e06dbdd5c1780aa5c818ca5cf4b7c3558253ecaed8069f303987576d

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 232,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0xbc14f660e06dbdd5c1780aa5c818ca5cf4b7c3558253ecaed8069f303987576d",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/232.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/232.md)


### Technical Analysis
We verified that the payload is adding the declared bridge adapters on Ethereum for the Celo network in the correct role - forwarder as described in the IPFS.
We further verified the addresses on Celo and the configured receivers there against the addresses configured in the payload for the forwarder.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.