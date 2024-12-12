# Proposal 216. Increase Borrow Slope1 to all Stablecoins across all Aave Instances

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=216)

### Governance Forum Discussions
[Link to forum discussions](https://governance.aave.com/t/arfc-increase-borrow-slope1-to-all-stablecoins-across-all-aave-instances/19979)

### Payloads

* Ethereum v2 - [proposal payloads](https://etherscan.io/address/0xC2C67Ce19924D5beFd42A3fB96f5E01D3aCdAe17)

* Ethereum v3 - [proposal payloads](https://etherscan.io/address/0xd8c8fC05d5a5e5a04B527aBAeA0110624D4FfBc5)

* Ethereum Lido  - [proposal payloads](https://etherscan.io/address/0x772C2a2aA905363D9958bCfd4f6891fc876dCA44)

* Ethereum EtherFi - [proposal payloads](https://etherscan.io/address/0xE5a064E8380Dd6984562d207542f2CF036Ae887E)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x5f8bad9BE248C4288E74dEE0A1311D7595a81d9C)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x41Fad3911a819646FF385e392AD05046e64661F8)

* OP Mainnet - [proposal payloads](https://optimistic.etherscan.io/address/0x41A66C5aF61F71cF33b6a1Ceb2caA911Aef4EfAa)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0x725D260e90765fA7662a42c7745b7b333855acA9)

* Metis - [proposal payloads](https://explorer.metis.io/address/0x2481f10CbeAfD144f192D84e70b784084066D943)

* Base - [proposal payloads](https://basescan.org/address/0x40B3b943b063C901457E2cd14e3054118C942827)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x2679BF679Cc73C8e7809F6a944Dd8aBd2fA18805)

* Scroll - [proposal payloads](https://scrollscan.com/address/0x9d9892256dF8f97d0c15F4494aa5D44D376CC749)

* BNB Smart Chain - [proposal payloads](https://bscscan.com/address/0x5a43ebA724b45B79d105eE5471219DB9A48Da3cF)

* zkSync Era - [proposal payloads](https://era.zksync.network/address/0xBF9Cb1382b612Eb89F77dc7f97472c16D6e33147)



## Certora Analysis

### Proposal Types
* :wrench: :bar_chart: Configuration updates

### Context
This proposal seeks to increase the borrow slope1 parameter for stablecoins across all Aave V3 and V2 instances to 12.5%, aligning interest rate models with the updated Stable Debt Reserve (SDR) strategy. The adjustment aims to optimize protocol revenue, enhance capital efficiency, and ensure appropriate risk compensation for lenders amid rising stablecoin utilization. By adapting to current market conditions, this change promotes sustainability and competitiveness across Aave’s ecosystem.

### Proposal Creation
Transaction: [0x0baff0c72577e0843d68fe60d4abae5b44c7d0f145c805bc8e1ba0b223e76a0e](https://etherscan.io/tx/0x0baff0c72577e0843d68fe60d4abae5b44c7d0f145c805bc8e1ba0b223e76a0e)
- `proposalId`: 216
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x1dea9e7846d661c189e2a5046ec5b7b0bfc395fcf87ba3fad25f1583adea910b

**`createProposal()` Parameters**
```
{
    "payloads": [
        {
            "chain": "1",
            "accessLevel": 1,
            "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            "payloadId": 220
        },
        {
            "chain": "137",
            "accessLevel": 1,
            "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            "payloadId": 92
        },
        {
            "chain": "43114",
            "accessLevel": 1,
            "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            "payloadId": 61
        },
        {
            "chain": "10",
            "accessLevel": 1,
            "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
            "payloadId": 60
        },
        {
            "chain": "42161",
            "accessLevel": 1,
            "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            "payloadId": 65
        },
        {
            "chain": "1088",
            "accessLevel": 1,
            "payloadsController": "0x2233F8A66A728FBa6E1dC95570B25360D07D5524",
            "payloadId": 30
        },
        {
            "chain": "8453",
            "accessLevel": 1,
            "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            "payloadId": 47
        },
        {
            "chain": "100",
            "accessLevel": 1,
            "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
            "payloadId": 38
        },
        {
            "chain": "534352",
            "accessLevel": 1,
            "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE",
            "payloadId": 28
        },
        {
            "chain": "56",
            "accessLevel": 1,
            "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627",
            "payloadId": 28
        },
        {
            "chain": "324",
            "accessLevel": 1,
            "payloadsController": "0x2E79349c3F5e4751E87b966812C9E65E805996F1",
            "payloadId": 9
        }
    ],
    "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    "ipfsHash": "0x1dea9e7846d661c189e2a5046ec5b7b0bfc395fcf87ba3fad25f1583adea910b"
}
```

### Aave Seatbelt Report
**Proposal Report**
[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/216.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/220.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/92.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/61.md)

* OP Mainnet - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/60.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/65.md)

* Metis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/30.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/47.md)

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/38.md)

* Scroll - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/28.md)

* BNB Smart Chain - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/28.md)

* zkSync Era - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/324/0x2E79349c3F5e4751E87b966812C9E65E805996F1/9.md)


### Technical Analysis
This analysis ensures that all borrow slope1 and slope2 parameters in the payloads match the intended values specified in the proposal for all Aave instances and markets. By cross-referencing the deployed values with the proposal and conducting both automated and manual validation checks, we confirm full alignment with the intended changes. This thorough verification guarantees that the adjustments are correctly implemented to support the protocol’s objectives.
The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.