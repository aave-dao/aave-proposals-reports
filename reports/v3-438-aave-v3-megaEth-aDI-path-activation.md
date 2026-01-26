# Proposal 438. MegaEth aDI path activation

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=438)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/technical-maintenance-proposals/15274/124)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x790E087A98C0552F6Ca5b85be513551a8DE188d4)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking


### Context
Proposal to register the necessary MegaEth adapters on a.DI, a technical pre-requirement for an activation vote of Aave v3 MegaEth.

### Proposal Creation
Transaction: [0xf7b18456d6d0d3186fb7ed2e4f8636129c36e834a7247e2403f01d5578bddb01](https://etherscan.io/tx/0xf7b18456d6d0d3186fb7ed2e4f8636129c36e834a7247e2403f01d5578bddb01)
- `proposalId`: 438
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0xee8234ef03e0fecc033a0eb8322ac88347aa49ccf5f0a73a4f642057fc0e4572

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 395,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xee8234ef03e0fecc033a0eb8322ac88347aa49ccf5f0a73a4f642057fc0e4572",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/438.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/395.md)


### Technical Analysis

We have verified the code at the `Aave Governance deployment` addresses.     We have validated that the cross-chain controllers registered on the adapters are as specified. We have checked the chain_id and confirmed that the new bridging path uses the correct adapters. We have validated the payload logic.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.