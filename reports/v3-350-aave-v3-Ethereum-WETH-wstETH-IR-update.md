# Proposal 350. Interest Rate Update - WETH and wstETH Ethereum

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=350)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/risk-stewards-interest-rate-update-weth-and-wsteth-ethereum/22625)

### Payloads

* Ethereum Core - [proposal payloads](https://etherscan.io/address/0x8D12a1f8204Aa3DF750050c44099b2d35ae1b481)

* Ethereum Prime - [proposal payloads](https://etherscan.io/address/0x1f7d4D221FB9B9C09821F9a4a5bEA7683175c61C)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
This publication proposes updating the WETH and wstETH Interest Rate configuration on both Core and Prime instances of Aave v3 on Ethereum.

### Proposal Creation
Transaction: [0x7a931f8d2b4c029fee0f3a3eca8399fc7da193b82cc579257ca6a6bff1ed6046](https://etherscan.io/tx/0x7a931f8d2b4c029fee0f3a3eca8399fc7da193b82cc579257ca6a6bff1ed6046)
- `proposalId`: 350
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x959fd9535907af7498eebee9aa3475d126ff94d2aa5dbd3f6339e894e582a009

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 323,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x959fd9535907af7498eebee9aa3475d126ff94d2aa5dbd3f6339e894e582a009",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/350.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/323.md)



### Technical Analysis
We have verified that only the parameters mentioned in the specification table have been modified to the correct amounts with respect to precision.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.