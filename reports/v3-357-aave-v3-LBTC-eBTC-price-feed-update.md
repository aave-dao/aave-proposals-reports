# Proposal 357. LBTC and eBTC Price Feeds Update

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=357)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-lbtc-oracle-and-capo-implementation-update/22614)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x399DF0195aF9815C4870f8E7961a6038265086Ac)

* Base - [proposal payloads](https://basescan.org/address/0x55890cbaF4b3d3Ba485624533f7C8eC1E665837B)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates

### Context
AIP for updating the price feeds of LBTC and eBTC, ensuring accurate prices for both assets that will be upgraded to yield-bearing tokens.

### Proposal Creation
Transaction: [0x44dc2e867f4794f36d23501e7d058790317b3472e129f023844cc3697619e387](https://etherscan.io/tx/0x44dc2e867f4794f36d23501e7d058790317b3472e129f023844cc3697619e387)
- `proposalId`: 357
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x7329a0af8ab3047c6147120a143571c78519feb346a649c930baa3814adaeeb5

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 328,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 84,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x7329a0af8ab3047c6147120a143571c78519feb346a649c930baa3814adaeeb5",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/357.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/328.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/84.md)


### Technical Analysis
We have verified the correct addresses were configured as the price feeds with the correct configuration.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.