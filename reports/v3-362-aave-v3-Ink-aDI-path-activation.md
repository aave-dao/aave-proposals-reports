# Proposal 362. Ink aDI path activation

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=362)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/technical-maintenance-proposals/15274/108)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x9cdA84ae11d829079EDcCaEd49e473f6fb841b75)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking


### Context
Proposal to register the necessary Ink adapters on a.DI, a technical pre-requirement to have Aave Governance-controlled contracts on Ink, in this case, cross-chain GHO-related to be listed on the Aave <> Ink friendly fork.

### Proposal Creation
Transaction: [0x44ebb2a858afbdff82f1d882a893dcf90a6a1aedae3140814e8242f2132c54c0](https://etherscan.io/tx/0x44ebb2a858afbdff82f1d882a893dcf90a6a1aedae3140814e8242f2132c54c0)
- `proposalId`: 362
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x20bb1e0d65a57197ff4c69c2b8057149f5e50302ff01f58851e5d3ea1c7bf937

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 332,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x20bb1e0d65a57197ff4c69c2b8057149f5e50302ff01f58851e5d3ea1c7bf937",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/362.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/332.md)


### Technical Analysis
We have verified the addresses related to the proposal for correctness. We have confirmed the proposal logic is correct.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.