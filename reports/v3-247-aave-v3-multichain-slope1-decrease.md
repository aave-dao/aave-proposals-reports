# Proposal 247. Decrease Slope1 Parameter for Stablecoins on Aave V3

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=247)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-chaos-labs-risk-stewards-decrease-slope1-parameter-for-stablecoins-on-aave-v3-01-29-25/20841)

### Payloads

* Ethereum Core - [proposal payloads](https://etherscan.io/address/0xE9DdbCeDF0496A4c044C0F7b44491B64d266296c)

* Ethereum Prime - [proposal payloads](https://etherscan.io/address/0x4DA79d2f5A4f63502B230F3F4586D0fd5b2b718a)

* Ethereum EtherFi - [proposal payloads](https://etherscan.io/address/0x272d588EfcDe85aC6Cb4fEfC0a330b5C26e396d7)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x586D50BE365f8b8BbD47CE9e3532470A41A80F93)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x118e5B162915FD6236dbB38A7Fc95EE382f0C56b)

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0x0761bc3e4716790677cB0E4FCBF29A7fE614C6aE)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x1De69daBD3552f1Eb70De602313f271346FC5307)

* Metis - [proposal payloads](https://explorer.metis.io/address/0xf907b1F349d235C7fcF93Da796b2F6a544D7E00a)

* Base - [proposal payloads](https://basescan.org/address/0xeE3f1B7Ef5f34Ab5380930a5C1c21Ed731500af6)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x7742057a9C2CFffFfa54bD25fb571849aAB087D6)

* Scroll - [proposal payloads](https://scrollscan.com/address/0x183Dd10eE325428a7561344f12924719720d636a)

* BNB Smart Chain - [proposal payloads](https://bscscan.com/address/0x40Ed913dd3F5798F5945Aa83A65C00776E03C706)

* zkSync - [proposal payloads](https://era.zksync.network/address/0xb3B2c7E8F6f86EFa92AA2B1663F161577BB3bf02)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
In light of recent market changes, Chaos Labs recommends setting the target borrow rate for all stablecoins to 9.50%.

### Proposal Creation
Transaction: [0xb39d22acc4396ca526c7997e104b8e923617786bcabff314ef4a688cbfa980e4](https://etherscan.io/tx/0xb39d22acc4396ca526c7997e104b8e923617786bcabff314ef4a688cbfa980e4)
- `proposalId`: 247
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xb402faa8be19367e6354f3be2044145c06a997cdc1a365f30de5807f1ea17998

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 244,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 99,
        },
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 68,
        },
        {
            chain: "10",
            payloads_controller: "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
            payload_id: 66,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 74,
        },
        {
            chain: "1088",
            payloads_controller: "0x2233F8A66A728FBa6E1dC95570B25360D07D5524",
            payload_id: 34,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 56,
        },
        {
            chain: "100",
            payloads_controller: "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
            payload_id: 45,
        },
        {
            chain: "534352",
            payloads_controller: "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE",
            payload_id: 35,
        },
        {
            chain: "56",
            payloads_controller: "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627",
            payload_id: 32,
        },
        {
            chain: "324",
            payloads_controller: "0x2E79349c3F5e4751E87b966812C9E65E805996F1",
            payload_id: 13,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0xb402faa8be19367e6354f3be2044145c06a997cdc1a365f30de5807f1ea17998",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/247.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/244.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/99.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/68.md)

* Optimism - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/66.md)

* Arbitrum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/74.md)

* Metis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/34.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/56.md)

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/45.md)

* Scroll - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/35.md)

* BNB Smart Chain - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/32.md)

* zkSync - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/324/0x2E79349c3F5e4751E87b966812C9E65E805996F1/13.md)


### Technical Analysis
We have verified that all parameters are configured to the specified percentages in the ipfs document—9.50% for standard stablecoins and 10.50% for bridged stablecoins. The ipfs configuration also includes additional assets (e.g., USDC.e, DAI.e, USDbC, and USD//C) that are not mentioned in the forum version. This discrepancy has been acknowledged; however, it does not affect the core recommendation, as the target percentages remain consistent across both versions.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.