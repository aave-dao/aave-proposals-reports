# Proposal 368. Add Fluid Protocol to flashBorrowers

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=368)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-add-fluid-protocol-to-flashborrowers/23007)

### Payloads

* Polygon - [proposal payloads](https://polygonscan.com/address/0xB68A43cA14e4Fb495823201004CE631479Dee8e4)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xB68A43cA14e4Fb495823201004CE631479Dee8e4)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
Adding fluid protocol as flashborrower with no fee.

### Proposal Creation
Transaction: [0x1d796ee4bebc7b50b1f86d908bf9453a9f88de5a65cd8a8172ade2a717417c2a](https://etherscan.io/tx/0x1d796ee4bebc7b50b1f86d908bf9453a9f88de5a65cd8a8172ade2a717417c2a)
- `proposalId`: 368
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xb7ce06bba8767b2dc12dde8ad1f6c31d4cb7b24136291548deca84a2228c09d8

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 126,
        },
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 93,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xb7ce06bba8767b2dc12dde8ad1f6c31d4cb7b24136291548deca84a2228c09d8",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/368.md)

**Payload Reports**

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/126.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/93.md)


### Technical Analysis
We have verified the address specified and approve the overall logic compare to intention.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.