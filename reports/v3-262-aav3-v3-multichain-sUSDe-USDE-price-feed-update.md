# Proposal 262. sUSDe and USDe Price Feed Update

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=262)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-susde-and-usde-price-feed-update/20495)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x09b9a2D4190668cD53D66ef60243C93c8538DeEc)

* Ethereum Lido - [proposal payloads](https://etherscan.io/address/0xF64a47956eCd99f8Cd0495fc2B15051D33d3a893)

* zkSync Era - [proposal payloads](https://era.zksync.network/address/0x115eD8ff4Eec1A02bB74056460FCaD2557870a8c)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
This proposal suggests hardcoding the USDe price to match the USDT price in Aave’s pricing feeds. By linking USDe’s value directly to USDT, we align the sUSDe oracle with USDT pricing, ensuring seamless integration and avoiding disruptions caused by transient price fluctuations in USD

### Proposal Creation
Transaction: [0xc087a2b87596192a40b50478c7ed8e566a6bcbd18f0f2721e7d442199d7ce700](https://etherscan.io/tx/0xc087a2b87596192a40b50478c7ed8e566a6bcbd18f0f2721e7d442199d7ce700)
- `proposalId`: 262
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xd66c72d90cb2160fa50614ea18e83efe4e55f1e1ce481ac099d45c807906faa5

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 254,
        },
        {
            chain: "324",
            payloads_controller: "0x2E79349c3F5e4751E87b966812C9E65E805996F1",
            payload_id: 16,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0xd66c72d90cb2160fa50614ea18e83efe4e55f1e1ce481ac099d45c807906faa5",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/262.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/254.md)

* Ethereum 2 - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/254.md)

* zkSync Era - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/324/0x2E79349c3F5e4751E87b966812C9E65E805996F1/16.md)


### Technical Analysis
We have confirmed that the price feeds refer to usdt now as there base aggregator and, the price providers remain correct.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.