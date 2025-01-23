# Proposal 234. Update Lido GHO base borrow rate

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=234)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-risk-stewards-reduce-gho-borrow-rate-prime-instance/20501)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x88be0A1D8F72e2b361Ec370bD487eD3F8B03AA9F)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
This publication proposes reducing the base borrow rate Parameter for the GHO Reserve on Prime instance by 2.00%.

### Proposal Creation
Transaction: [0xadd1dd527b9d11e2ef2d6b0e4533cb94ef55e45b6c8cb0bcafdfce8a58c4d749](https://etherscan.io/tx/0xadd1dd527b9d11e2ef2d6b0e4533cb94ef55e45b6c8cb0bcafdfce8a58c4d749)
- `proposalId`: 234
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x7c96588d84f5188e19ccbe659c40030e238e76e0fa1785af02d77ce733f4c917

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 235,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0x7c96588d84f5188e19ccbe659c40030e238e76e0fa1785af02d77ce733f4c917",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/234.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/235.md)


### Technical Analysis
We have reviewed the proposal and confirmed that the base borrow rate of GHO on the prime instance has been updated to 8.5% as specified in the ipfs and the forum.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.