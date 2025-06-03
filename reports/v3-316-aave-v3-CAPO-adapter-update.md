# Proposal 316. CAPO Adapter Maintenance Update

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=316)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/technical-maintenance-proposals/15274/55)

### Payloads

* Ethereum Core - [proposal payloads](https://etherscan.io/address/0x17E0C68Ff000d16cdAA4b5150bBFf57CF011ad48)

* Ethereum Prime - [proposal payloads](https://etherscan.io/address/0xB2953628a8aB2B7157b2f06B7544e4EF88352417)

* Ethereum EtherFi - [proposal payloads](https://etherscan.io/address/0xE02F0b6fdF953e76a736428d1F0d70920d53193D)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x96B342B33DB32f42F568e6ab5dA9994EE742c5C6)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xdcC41C8d50b661222F3840b67D8Fd7FaFB0BDb90)

* OP Mainnet - [proposal payloads](https://optimistic.etherscan.io/address/0x60693cf6eACE94339bd072d4629d94125fBf367c)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0x5C1dA3a21A57a6a787182CfF56EC0a958eCCb911)

* Metis - [proposal payloads](https://explorer.metis.io/address/0xA45bEa1c37563cBb9E3BF44edDefc9B2C30E5Bf8)

* Base - [proposal payloads](https://basescan.org/address/0x81DF07Eed2C0e257E02C9D08Edde32ccDb6E9692)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x0A120970B44e20F3A80b4e7995f55ae4acc7D797)

* Scroll - [proposal payloads](https://scrollscan.com/address/0x6835065D10e26d3609241E93c25A0a9D21070A85)

* BNB Smart Chain - [proposal payloads](https://bscscan.com/address/0xE21c3B4C0000664B1124e421d986EbA26ff40414)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
Maintenance proposal to update stable price cap adapters across all v2 and v3 instances to the latest version. The sDAI adapters on Ethereum and Gnosis Aave instances are also updated from non-capo to capo adapters, and USDS adapters are updated to use USDS/USD feed from the previous DAI/USD feed, given that liquidity of USDS is perfectly normalized.

### Proposal Creation
Transaction: [0x82ca5a7707a74b449f43f9ebb1c0b8b7dd31c16b5172c7e204c5324be49b81f3](https://etherscan.io/tx/0x82ca5a7707a74b449f43f9ebb1c0b8b7dd31c16b5172c7e204c5324be49b81f3)
- `proposalId`: 316
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0xf77f1206b8b2ae21cd110abe44848a6280efe3584d6d9e4e3bef84c7a9d15095

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 292,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 112,
        },
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 79,
        },
        {
            chain: "10",
            payloads_controller: "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
            payload_id: 76,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 89,
        },
        {
            chain: "1088",
            payloads_controller: "0x2233F8A66A728FBa6E1dC95570B25360D07D5524",
            payload_id: 39,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 71,
        },
        {
            chain: "100",
            payloads_controller: "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
            payload_id: 53,
        },
        {
            chain: "534352",
            payloads_controller: "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE",
            payload_id: 42,
        },
        {
            chain: "56",
            payloads_controller: "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627",
            payload_id: 39,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xf77f1206b8b2ae21cd110abe44848a6280efe3584d6d9e4e3bef84c7a9d15095",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/316.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/292.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/112.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/79.md)

* OP Mainnet - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/76.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/89.md)

* Metis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/39.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/71.md)

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/53.md)

* Scroll - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/42.md)

* BNB Smart Chain - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/39.md)


### Technical Analysis
We have validated a 1 to 1 match to the specifications and forum regarding the assets specified to be changed.
The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.