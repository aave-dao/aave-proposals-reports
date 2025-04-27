# Proposal 299. Onboard PT sUSDe July and PT eUSDe May on Core Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=299)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-onboard-susde-july-expiry-pt-tokens-on-aave-v3-core-instance/21878)

### Payloads

* Ethereum 1 - [proposal payloads](https://etherscan.io/address/0x6C1Aa437555221138c15eD5f5fd496CAcA9ff373)

* Ethereum 2 - [proposal payloads](https://etherscan.io/address/0x6e357144B1D220c448dEA7bc711Ca417e0DF66c6)

* Ethereum 3 - [proposal payloads](https://etherscan.io/address/0xE90AF55B07Fb0F27f5D8F63040441b8cc97E5172)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets

### Context
This proposal seeks to onboard pendle [PT-sUSDe-31July2025](https://etherscan.io/address/0x3b3fB9C57858EF816833dC91565EFcd85D96f634) and [PT-eUSDe-29May2025](https://etherscan.io/address/0x50D2C7992b802Eef16c04FeADAB310f31866a545) on the Aave V3 core instance and activate Edge AGRS system to automate updating eMode category params for these assets.

### Proposal Creation
Transaction: [0x7bffd694a0d2d46c85bf873126bba7e20785ad9a0a995dfc1566d96bc93504be](https://etherscan.io/tx/0x7bffd694a0d2d46c85bf873126bba7e20785ad9a0a995dfc1566d96bc93504be)
- `proposalId`: 299
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x3af2cc97ce1e3eefdf9ce221ab696f677ae27916b2450d538f82f2181e570057

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 274,
        },
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 275,
        },
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 276,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x3af2cc97ce1e3eefdf9ce221ab696f677ae27916b2450d538f82f2181e570057",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/299.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/274.md)

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/275.md)

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/276.md)


### Technical Analysis
We have verified the risk parameters that were specified are the same as listed. We have checked and verified both emode 8 and 9 were whitelisted to the AGRS. The label name of PT eUSDe is configured correctly with a capital E as in the underlying asset name.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.