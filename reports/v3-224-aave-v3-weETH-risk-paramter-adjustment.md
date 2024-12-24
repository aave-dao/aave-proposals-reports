# Proposal 224. weETH Risk Parameter Adjustment

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=224)

### Governance Forum Discussions
[Link to forum discussions](https://governance.aave.com/t/arfc-weeth-risk-parameter-adjustment/20167)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x75F2CEf2A4e3CF520437eD8b6D8b6ba771631349)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates

### Context
A proposal to adjust weETH’s LTV, LT, and LB on the Ethereum Core instance.
weETH’s collateral parameters are currently set to 72.5%, 75%, and 7.5% for LTV, LT, and LB, respectively, on Ethereum — Core. Following observations of user behavior and on-chain liquidity, we are able to recommend adjusting these parameters to make the asset more efficient as collateral. The vast majority of debt against weETH is WETH, making these positions low-risk due to weETH’s utilization of the ETH/USD oracle augmented with its exchange rate.

### Proposal Creation
Transaction: [0xf0ff5a3663e33f583ec0c8733d1b9a1b92bba654113b512377300880138f9636](https://etherscan.io/tx/0xf0ff5a3663e33f583ec0c8733d1b9a1b92bba654113b512377300880138f9636)
- `proposalId`: 224
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xa4da1c686491e35541aa7e2659d55d0b93e395a89d1b268981aec3b8b2227bc1

**`createProposal()` Parameters**
```
{
    "payloads": [
        {
            "chain": "1",
            "accessLevel": 1,
            "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            "payloadId": 227
        }
    ],
    "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    "ipfsHash": "0xa4da1c686491e35541aa7e2659d55d0b93e395a89d1b268981aec3b8b2227bc1"
}
```

### Aave Seatbelt Report
**Proposal Report**
[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/224.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/227.md)


### Technical Analysis
We have reviewd the specified parameters have changed to desired numbers. 

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.