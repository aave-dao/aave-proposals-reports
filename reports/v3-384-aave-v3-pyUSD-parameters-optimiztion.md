# Proposal 384. pyUSD Parameters Optimization

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=384)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-pyusd-parameters-optimization/23082/3)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x4EdC649be130D1C8B841629572874eD4E682F353)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
This proposal updates the pyUSD reserve configuration on Ethereum v3 Core.

### Proposal Creation
Transaction: [0x675804e5bdf833350d1655598935d1be77662192becfdbfd201d1b138ff4ba42](https://etherscan.io/tx/0x675804e5bdf833350d1655598935d1be77662192becfdbfd201d1b138ff4ba42)
- `proposalId`: 384
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x7f8ccb2b8643eb7170a5413b5c01ac5cf1e199f92ea39eb35850d8ae98f7f07e

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 352,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x7f8ccb2b8643eb7170a5413b5c01ac5cf1e199f92ea39eb35850d8ae98f7f07e",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/384.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/352.md)


### Technical Analysis
We have verified the changes to the risk parameters match the description of the IPFS and forum and no further actions have been made.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.