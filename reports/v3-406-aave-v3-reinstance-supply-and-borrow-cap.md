# Proposal 406. Reinstate Supply and Borrow Caps on Aave V3 Gnosis Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=406)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-reinstate-supply-and-borrow-caps-on-aave-v3-gnosis-instance/23373)

### Payloads

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0xd52006e40C7e98E69A456B089b16aF6fAfe63032)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
The Gnosis protocol team has communicated its intention to reopen the canonical bridge, prompting us to initiate the governance process to restore the decreased caps. Specifically, we propose to reverse the previously implemented freeze of all assets on the Gnosis Chain, restoring the supply and borrow caps to levels that marginally exceed the current supply and borrow balances.

### Proposal Creation
Transaction: [0x62c913205a80d6609b709c20d128c24592d963a2e0b1087abc1d530dd943f754](https://etherscan.io/tx/0x62c913205a80d6609b709c20d128c24592d963a2e0b1087abc1d530dd943f754)
- `proposalId`: 406
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x67eed08af16e273247455ed3712df3f6317cb95e85feec6fb9fd9f68c295a8aa

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "100",
            payloads_controller: "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
            payload_id: 66,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x67eed08af16e273247455ed3712df3f6317cb95e85feec6fb9fd9f68c295a8aa",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/406.md)

**Payload Reports**

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/66.md)


### Technical Analysis
We have verified that the updated risk params matching between the IPFS, payload and the forum. We have validate seatbelt execution of the payload.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.