# Proposal 405. Safety Module Emissions Update

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=405)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-amend-safety-module-emissions/16640/27)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x9AB426D56B949A7313f4d09f0d14Dc8F930D2D7f)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
Re-enable stkBPT and stkAAVE incentives emissions for 90 days after previous period ended. Add allowance for stkBPT V1 holders who have unclaimed amounts.

### Proposal Creation
Transaction: [0x9da7643759e5e60f4078f429d0a6a62e9b07aca21ed14349af13aa9425e437ed](https://etherscan.io/tx/0x9da7643759e5e60f4078f429d0a6a62e9b07aca21ed14349af13aa9425e437ed)
- `proposalId`: 405
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x2bd4b997a994d08aa01e0fbf4708eee0a418dd857414dfc3bcf63a3a08b773ac

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 368,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x2bd4b997a994d08aa01e0fbf4708eee0a418dd857414dfc3bcf63a3a08b773ac",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/405.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/368.md)


### Technical Analysis

We have confirmed alignment between the forum post, the IPFS content, and the on-chain payload.
We have verified the relevant addresses, allowances amounts and duration. With regarding to decimal precision. We confirmed payload's logic and validated the execution via seatbelt. 

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.