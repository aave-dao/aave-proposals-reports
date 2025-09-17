# Proposal 376. Raise sUSDe and USDe November expiry PT tokens caps on Aave V3 Core Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=376)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-raise-susde-and-usde-november-expiry-pt-tokens-caps-on-aave-v3-core-instance/23117)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xE1c46CA14cd856D333Bf657e1d3B978E6089F4B6)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
This ARFC proposes to increase supply caps on sUSDe November expiry PT tokens on Aave V3 Core Instance in anticipation of the PT rollover in September.

### Proposal Creation
Transaction: [0x1ca60c5ee8684b29d86ebb7d519ef72b4e9105a91a4d3e4ceaeed22630a8f553](https://etherscan.io/tx/0x1ca60c5ee8684b29d86ebb7d519ef72b4e9105a91a4d3e4ceaeed22630a8f553)
- `proposalId`: 376
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x126974bde627cbc93918a913845077a08ec78ae04bdf49d5da15b41478e157b4

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 341,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x126974bde627cbc93918a913845077a08ec78ae04bdf49d5da15b41478e157b4",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/376.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/341.md)


### Technical Analysis
We have confirmed the caps have increased correctly to the correct amount for the correct asset.
The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.