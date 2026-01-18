# Proposal 435. stkABPT Emission Update

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=435)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-safety-module-umbrella-emission-update/23103/9)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x90Aa17cb8B78C85DE0C781d61aCE30e4686e7803)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates


### Context

Reduce AAVE emissions for the legacy Safety Module stkABPT (stkAAVE/wstETH BPTv2) from 130 AAVE/day to 40 AAVE/day.

### Proposal Creation
Transaction: [0xf3ffdbde551dcfa397690d7130b78140f2773dbe2796f907c26e443b10671d29](https://etherscan.io/tx/0xf3ffdbde551dcfa397690d7130b78140f2773dbe2796f907c26e443b10671d29)
- `proposalId`: 435
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x67acac178fa108114611d99c85b9efda1928ccec8d836a1dda54dbb809d042cf

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 388,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x67acac178fa108114611d99c85b9efda1928ccec8d836a1dda54dbb809d042cf",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/435.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/388.md)


### Technical Analysis

We have verified that the emission rate is correct with respect to decimal precision.
We have validated the new distribution end date and the updated allowance.
We reviewed the payload logic and validated the intended execution via the Seatbelt simulation.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.