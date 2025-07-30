# Proposal 348. Fire drill proposal Avalanche VotingMachine

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=348)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/technical-maintenance-proposals/15274/92)

### Payloads

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xFb9BaA51b2A1f721B3FeAD9A9Af081B7856EE5Bc)



## Certora Analysis

### Context
Do a fire drill voting flow with a mock governance proposal using Avalanche as the voting network instead of Polygon as usual, to test that all peripheral systems are properly functioning.

### Proposal Creation
Transaction: [0xfddc79ff5f9334da1a2673066a2a60d3e00003d956718bc54099e8af88ae9a8f](https://etherscan.io/tx/0xfddc79ff5f9334da1a2673066a2a60d3e00003d956718bc54099e8af88ae9a8f)
- `proposalId`: 348
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x70764c71c536a84acb96dd6e6e612eca166c29a0982fadd2ecb9d8cd6dca6c02

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 91,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x70764c71c536a84acb96dd6e6e612eca166c29a0982fadd2ecb9d8cd6dca6c02",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/348.md)

**Payload Reports**

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/91.md)


### Technical Analysis
We have verified the proposal is only checking the voting portal is properly functioning.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.