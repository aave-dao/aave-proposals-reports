# Proposal 385. Safety Module & Umbrella Emission Update

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=385)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-safety-module-umbrella-emission-update/23103/8)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xF8a9d7cAb2Fc2dd4b5039C78C5A1881eF4656077)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking

* :wrench: :bar_chart: Configuration updates

### Context
This proposal outlines the next incremental reduction in Safety Module emissions.
 
### Proposal Creation
Transaction: [0x9803252ebd2674af29ed46368cda882747856979b211796323e730a10714bfe3](https://etherscan.io/tx/0x9803252ebd2674af29ed46368cda882747856979b211796323e730a10714bfe3)
- `proposalId`: 385
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xf03f91e0c1a9cc49a0c832145344699fba074eddee8175f3e70bb2e604f9db2e

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 353,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xf03f91e0c1a9cc49a0c832145344699fba074eddee8175f3e70bb2e604f9db2e",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/385.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/353.md)


### Technical Analysis
We have verified the use of the correct functions to the correct assets for the correct amounts.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.