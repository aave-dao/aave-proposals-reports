# Proposal 353. Upgrade Aave instances to v3.5

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=353)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-bgd-aave-v3-5-v3-4-part-2/22639/1)

### Payloads

* Ethereum core - [proposal payloads](https://etherscan.io/address/0xD51B0B941cfcF3388c17ABa5DcBab766d34fD45b)

* Ethereum prime - [proposal payloads](https://etherscan.io/address/0x6ab8c847371911C778963Fa0C07645f3e587B012)

* Ethereum etherfi - [proposal payloads](https://etherscan.io/address/0xb705bdF5DF2c8658e3C3f3bdcCA6084000C026d3)

* Ethereum 4 - [proposal payloads](https://etherscan.io/address/0xfea1ae0b74FDBD61CEF293CAA937e26AF597F176)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x27a69BE794648aa6A08E449490d60f1669aEd2e0)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xe02C2cDA7e2000D75dE8AE9A93A8151afA8186f4)

* OP Mainnet - [proposal payloads](https://optimistic.etherscan.io/address/0x93f16Fd74eF98e7652bA5C5aD844473Cbe7377A5)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0xC1a25A94cB35C4973BFD435CeAB6aeb800278584)

* Metis - [proposal payloads](https://explorer.metis.io/address/0x6fF38fBBD238b8363b04C0C54ffAE0622Bf1B289)

* Base - [proposal payloads](https://basescan.org/address/0x2865680741199B50870eD452fE9b590501791c87)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x32A1b4a26e0bA9164bc05eb764D3cd7337d431aD)

* Scroll - [proposal payloads](https://scrollscan.com/address/0x7467F305c2a269C22548C0821E6a33caa2C7Ec9B)

* BNB Smart Chain - [proposal payloads](https://bscscan.com/address/0x6d70Ed63F662f325135e4C97af2B030068f536B4)

* zkSync Era - [proposal payloads](https://era.zksync.network/address/0x1bC646CD1Fc56024f16B1Abf2197Fc0100c00Cf8)

* Linea - [proposal payloads](https://lineascan.build/address/0xc0799CF19914081684f0203cC87FE5436d5d717F)

* Celo - [proposal payloads](https://celo.blockscout.com/address/0xD8d64BAb7C362E5F762ea0E7c334801Fba604028)

* Sonic - [proposal payloads](https://sonicscan.org/address/0x85163f633bC6918a803C8D70791570D948b312Bc)



## Certora Analysis

### Proposal Types

* :scroll: :small_red_triangle: Contract upgrades



### Context
Upgrade the Aave protocol instances from v3.4 to v3.5.

### Proposal Creation
Transaction: [0x9c36b909d4de8458e0004d69e8916f6e362b6b320e2a2b24f89e867f512ce1dc](https://etherscan.io/tx/0x9c36b909d4de8458e0004d69e8916f6e362b6b320e2a2b24f89e867f512ce1dc)
- `proposalId`: 353
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x1c5a061ddf7d39473fd4fdc8fe6c4fc06285473f1db404335c1a5b392d1d9beb

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 317,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 123,
        },
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 89,
        },
        {
            chain: "10",
            payloads_controller: "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
            payload_id: 83,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 97,
        },
        {
            chain: "1088",
            payloads_controller: "0x2233F8A66A728FBa6E1dC95570B25360D07D5524",
            payload_id: 42,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 81,
        },
        {
            chain: "100",
            payloads_controller: "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
            payload_id: 56,
        },
        {
            chain: "534352",
            payloads_controller: "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE",
            payload_id: 45,
        },
        {
            chain: "56",
            payloads_controller: "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627",
            payload_id: 47,
        },
        {
            chain: "324",
            payloads_controller: "0x2E79349c3F5e4751E87b966812C9E65E805996F1",
            payload_id: 30,
        },
        {
            chain: "59144",
            payloads_controller: "0x3BcE23a1363728091bc57A58a226CF2940C2e074",
            payload_id: 11,
        },
        {
            chain: "42220",
            payloads_controller: "0xE48E10834C04E394A04BF22a565D063D40b9FA42",
            payload_id: 8,
        },
        {
            chain: "146",
            payloads_controller: "0x0846C28Dd54DEA4Fd7Fb31bcc5EB81673D68c695",
            payload_id: 7,
        },
        {
            chain: "1868",
            payloads_controller: "0x44D73D7C4b2f98F426Bf8B5e87628d9eE38ef0Cf",
            payload_id: 3,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x1c5a061ddf7d39473fd4fdc8fe6c4fc06285473f1db404335c1a5b392d1d9beb",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/353.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/317.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/123.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/89.md)

* OP Mainnet - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/83.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/97.md)

* Metis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/42.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/81.md)

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/56.md)

* Scroll - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/45.md)

* BNB Smart Chain - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/47.md)

* zkSync Era - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/324/0x2E79349c3F5e4751E87b966812C9E65E805996F1/30.md)

* Linea - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/59144/0x3BcE23a1363728091bc57A58a226CF2940C2e074/11.md)

* Celo - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42220/0xE48E10834C04E394A04BF22a565D063D40b9FA42/8.md)

* Sonic - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/146/0x0846C28Dd54DEA4Fd7Fb31bcc5EB81673D68c695/7.md)


### Technical Analysis
We have verified the new implementation is the same as the one reviewed by Certora. We have confirmed the upgrade logic is correct. We have verified the amount transferred to BGD. 

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.