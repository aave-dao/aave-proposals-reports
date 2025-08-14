# Proposal 354. Add tETH to Core Instance Ethereum

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=354)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-add-teth-to-core-instance-ethereum/22594/3)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x6994319Bb5954B643281d42F8487B728CdE38f24)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context
This publication proposes onboarding tETH as collateral to the Aave V3 Core Instance.


### Proposal Creation
Transaction: [0xd97cf88a4e75e920bd139476fbebda0e97ffc7e05b401c14444d78a38d8b40ed](https://etherscan.io/tx/0xd97cf88a4e75e920bd139476fbebda0e97ffc7e05b401c14444d78a38d8b40ed)
- `proposalId`: 354
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xceb7fe655d73f33159c4744ad02b1bba4010a7031f084f18425e893e318b99fa

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 327,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xceb7fe655d73f33159c4744ad02b1bba4010a7031f084f18425e893e318b99fa",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/354.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/327.md)


### Technical Analysis
We have verified the risk params match the IPFS and forum. We have validated the supply of the seed amount to the pool. We have checked the correctness of the price feed.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.