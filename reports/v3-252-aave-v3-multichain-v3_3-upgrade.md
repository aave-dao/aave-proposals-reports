# Proposal 252. Upgrade Aave instances to v3.3

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=252)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/bgd-aave-v3-3-feat-umbrella/20129)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x79691D2DFE962E4059F3b56B53D7Cc081F494aE0)

* Ethereum Lido - [proposal payloads](https://etherscan.io/address/0x5Deec870CAA11742BAE0f0B650EC8A549D1814Fa)

* Ethereum EtherFi - [proposal payloads](https://etherscan.io/address/0xceDd3bC91c502aA5d74eF4065fbBE5D0b5ECb4C3)

* Ethereum (transfer) - [proposal payloads](https://etherscan.io/address/0x5B1e57ceFa3BFCeA048306267C5029695315027a)

* Polygon - [proposal payloads](https://polygonscan.com/address/0xe39e928A82D3c4a406FfCAb671B3b36a21D98295)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x391095d2e79e7Bd89C1eb984220273268994a5b7)

* OP Mainnet - [proposal payloads](https://optimistic.etherscan.io/address/0x09262648Fce84992B68AbF216BfC47731F154462)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0x19ED0C564d7818BcA61C358b10f017F9239D2Df2)

* Metis - [proposal payloads](https://explorer.metis.io/address/0xb85d72EC1EfE48168c4aBC4eB855f8Cbcd05cE38)

* Base - [proposal payloads](https://basescan.org/address/0x1E81af09001aD208BDa68FF022544dB2102A752d)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0xCf85FF1c37c594a10195F7A9Ab85CBb0a03f69dE)

* Scroll - [proposal payloads](https://scrollscan.com/address/0xb77fc84a549ecc0b410d6fa15159C2df207545a3)

* BNB Smart Chain - [proposal payloads](https://bscscan.com/address/0x5E76E98E0963EcDC6A065d1435F84065b7523f39)

* zkSync Era - [proposal payloads](https://era.zksync.network/address/0xcE69DAb549C757432B7e4b62ec496fdc50a66218)

* Linea - [proposal payloads](https://lineascan.build//0x89654c66A6abd7174b525D05C2f4c442a615cee8)



## Certora Analysis

### Proposal Types

* :scroll: :small_red_triangle: Contract upgrades


### Context
This proposal will upgrade all active Aave instances to version v3.3.0.


### Proposal Creation
Transaction: [0xd8955658cc68d11fc2ffea0b779ea839e1b939ba24394e9665a51c6bd4719ec4](https://etherscan.io/tx/0xd8955658cc68d11fc2ffea0b779ea839e1b939ba24394e9665a51c6bd4719ec4)
- `proposalId`: 252
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x13c4f9441574b90e2210e9ca94a8632ba9d997eca6af66283932d3131d642894

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 249,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 98,
        },
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 67,
        },
        {
            chain: "10",
            payloads_controller: "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
            payload_id: 65,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 73,
        },
        {
            chain: "1088",
            payloads_controller: "0x2233F8A66A728FBa6E1dC95570B25360D07D5524",
            payload_id: 33,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 55,
        },
        {
            chain: "100",
            payloads_controller: "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
            payload_id: 44,
        },
        {
            chain: "534352",
            payloads_controller: "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE",
            payload_id: 34,
        },
        {
            chain: "56",
            payloads_controller: "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627",
            payload_id: 33,
        },
        {
            chain: "324",
            payloads_controller: "0x2E79349c3F5e4751E87b966812C9E65E805996F1",
            payload_id: 15,
        },
        {
            chain: "59144",
            payloads_controller: "0x3BcE23a1363728091bc57A58a226CF2940C2e074",
            payload_id: 4,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0x13c4f9441574b90e2210e9ca94a8632ba9d997eca6af66283932d3131d642894",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/252.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/249.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/98.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/67.md)

* OP Mainnet - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/65.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/73.md)

* Metis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/33.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/55.md)

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/44.md)

* Scroll - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/34.md)

* BNB Smart Chain - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/33.md)

* zkSync Era - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/324/0x2E79349c3F5e4751E87b966812C9E65E805996F1/15.md)

* Linea - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/59144/0x3BcE23a1363728091bc57A58a226CF2940C2e074/4.md)


### Technical Analysis
We have review that all the instances have been upgraded properly and consistently. We have verified that the code is identical to the github v3.3.0 repo upgrade. Additionally confirmed the A_USDC has been transfer properly to BGD Labs.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.