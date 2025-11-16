# Proposal 390. Allow PyUSD as collateral

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=390)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-enable-pyusd-as-collateral-on-aave-v2-core-instance/23235)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x3aacFD6b8e111C0eBd8de30d1A9eEc06E80F71ba)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
This AIP proposes to enable pyUSD as collateral on the V3 Core instance.

### Proposal Creation
Transaction: [0x90b83a6d65a74bed583c2c886080453defd4e96a9420f54bd0493ba67d509184](https://etherscan.io/tx/0x90b83a6d65a74bed583c2c886080453defd4e96a9420f54bd0493ba67d509184)
- `proposalId`: 390
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x3cfc7caf8a0bccfb08c45564f2c94dcaee7bee5471cf33abfb81c41e9334feaa

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 360,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x3cfc7caf8a0bccfb08c45564f2c94dcaee7bee5471cf33abfb81c41e9334feaa",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/390.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/360.md)


### Technical Analysis
We have verified the `LTV` configures to `75%` with respect to decimal precision, the update changes to the correct asset LTV.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.