# Proposal 223. USDS Interest Rate Curve Update

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=223)

### Governance Forum Discussions
[Link to forum discussions](https://governance.aave.com/t/arfc-usds-interest-rate-curve-update/20243)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x3eE2cbC6B8a0fBa025224aFcCe85A548f7daF01f)

* Ethereum Lido - [proposal payloads](https://etherscan.io/address/0xfFfC90a2B283F4A5f994034661606Fc21c31E0d5)


## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates

### Context
Chaos Labs recommends adjustments to USDS’s interest rate curves on the Prime and Core deployments. The frequent spikes have coincided with a decrease in borrows, as a result of large market outflows. To optimally price the asset, and to set USDS in line with other stablecoins, Chaos Labs recommend increasing the target borrow rate at UOptimal, which will also reduce the time spent above UOptimal. Specifically, Chaos Labs recommend targeting 12.5% at UOptimal and a Slope2 of 35% for both USDS markets, noting that this is aligned with the target rate for all other major stablecoin markets.

### Proposal Creation
Transaction: [0x0cda0efd5372e16500de349ed1d43cf0f47f380dd17ffc1c1bc64b791b42a9a6](https://etherscan.io/tx/0x0cda0efd5372e16500de349ed1d43cf0f47f380dd17ffc1c1bc64b791b42a9a6)
- `proposalId`: 223
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x70aac42c7fdd1833721a1e00bed7cdde16591bb66473849ba2eb5cc899106258

**`createProposal()` Parameters**
```
{
    "payloads": [
        {
            "chain": "1",
            "accessLevel": 1,
            "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            "payloadId": 226
        }
    ],
    "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    "ipfsHash": "0x70aac42c7fdd1833721a1e00bed7cdde16591bb66473849ba2eb5cc899106258"
}
```

### Aave Seatbelt Report
**Proposal Report**
[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/223.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/226.md)


### Technical Analysis
We have verified that the specified parameters has changed to the desired numbers. 

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.