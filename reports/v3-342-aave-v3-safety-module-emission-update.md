# Proposal 342. Safety Module Emission Update

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=342)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-safety-module-emission-update/22554)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x341Ba3Ee810dA1882126CbFBC35033caB6c30D00)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates

### Context
This publication outlines the next incremental reduction in AAVE emissions being distributed to stkAAVE and stkABPT holders.

### Proposal Creation
Transaction: [0x4fe815301e1e361ede1e48af8181c13ddb95aeaf1a6bd910c31d97ec9b3192a4](https://etherscan.io/tx/0x4fe815301e1e361ede1e48af8181c13ddb95aeaf1a6bd910c31d97ec9b3192a4)
- `proposalId`: 342
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x447c274d05b4c2dda0a18548f0bb9932e82f4574d38e60b77a28a1be2bd95cdd

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 319,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x447c274d05b4c2dda0a18548f0bb9932e82f4574d38e60b77a28a1be2bd95cdd",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/342.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/319.md)


### Technical Analysis
We have verified the reduction of the AAVE emissions to the correct amounts.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.