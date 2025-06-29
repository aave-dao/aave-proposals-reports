# Proposal 332. Discount Rate Risk Oracle Activation and update manual AGRS

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=332)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/technical-maintenance-proposals/15274/93)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x77242C29012708fC7Dd6d59008F5dFebb24332e3)

* Ethereum Prime - [proposal payloads](https://etherscan.io/address/0x5b730B35b3C72E23B01E0015B6425d87e18745D3)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x15d787228CF065dc77d18E773dab8102e20e32B9)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x4Ba8E4d02dCcad1a443FC8B1296Ca0194EbAd4b5)

* OP Mainnet - [proposal payloads](https://optimistic.etherscan.io/address/0x59ef87f23049374F6D4dB086982AFAc4Cf7b81AA)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0xda52975C8AAB4bfa46EF918a2088F338aF88FCf0)

* Metis - [proposal payloads](https://explorer.metis.io/address/0x4D9144Da88A9E81d9EACB29c7B5A0bBfBBc5c097)

* Base - [proposal payloads](https://basescan.org/address/0x0Aa5BB8D3038B93FBd080BD9eFe761efAC467afe)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x6BDCDCb5E995aA719089D0329381e2533f5e11c6)

* Scroll - [proposal payloads](https://scrollscan.com/address/0x5F784e558e3E946f1aDD0269208d415C5b3A606A)

* BNB Smart Chain - [proposal payloads](https://bscscan.com/address/0x53F247E6A237a8324a1154B3F424C063F19B3E60)

* zkSync Era - [proposal payloads](https://era.zksync.network/address/0xdee32259a89BA21f4aD1c992f3a7260644f906b4)

* Linea - [proposal payloads](https://lineascan.build//0x40b3aD48ffd85A84563e607069ba1C1DDC4716C3)

* Celo - [proposal payloads](https://celo.blockscout.com//0x48872dc471163148C699D5A9AFeE49Fa0C15102F)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
This proposal activates the automated Aave Generalised Risk Stewards (AGRS) system on the Ethereum core instance to perform automated discount rate updates on Pendle PT feeds. It also updates the manual AGRS to the most up-to-date iteration (already active on Ethereum), which allows for e-Mode category updates across all instances.

### Proposal Creation
Transaction: [0x4523dbad67240a6e95b6aca164dcd50faa3135805dc8d9e76e07ea2af468bb61](https://etherscan.io/tx/0x4523dbad67240a6e95b6aca164dcd50faa3135805dc8d9e76e07ea2af468bb61)
- `proposalId`: 332
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x90c865128c6c5162d7bf4d957fcf33a10a5da36ac6eef6a142299b8df2c2b7cc

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 309,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 115,
        },
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 84,
        },
        {
            chain: "10",
            payloads_controller: "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
            payload_id: 78,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 92,
        },
        {
            chain: "1088",
            payloads_controller: "0x2233F8A66A728FBa6E1dC95570B25360D07D5524",
            payload_id: 41,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 75,
        },
        {
            chain: "100",
            payloads_controller: "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
            payload_id: 55,
        },
        {
            chain: "534352",
            payloads_controller: "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE",
            payload_id: 44,
        },
        {
            chain: "56",
            payloads_controller: "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627",
            payload_id: 41,
        },
        {
            chain: "324",
            payloads_controller: "0x2E79349c3F5e4751E87b966812C9E65E805996F1",
            payload_id: 29,
        },
        {
            chain: "59144",
            payloads_controller: "0x3BcE23a1363728091bc57A58a226CF2940C2e074",
            payload_id: 10,
        },
        {
            chain: "42220",
            payloads_controller: "0xE48E10834C04E394A04BF22a565D063D40b9FA42",
            payload_id: 7,
        },
        {
            chain: "146",
            payloads_controller: "0x0846C28Dd54DEA4Fd7Fb31bcc5EB81673D68c695",
            payload_id: 5,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x90c865128c6c5162d7bf4d957fcf33a10a5da36ac6eef6a142299b8df2c2b7cc",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/332.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/309.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/115.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/84.md)

* OP Mainnet - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/78.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/92.md)

* Metis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/41.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/75.md)

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/55.md)

* Scroll - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/44.md)

* BNB Smart Chain - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/41.md)

* zkSync Era - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/324/0x2E79349c3F5e4751E87b966812C9E65E805996F1/29.md)

* Linea - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/59144/0x3BcE23a1363728091bc57A58a226CF2940C2e074/10.md)

* Celo - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42220/0xE48E10834C04E394A04BF22a565D063D40b9FA42/7.md)


### Technical Analysis
We have verified the address of the new Discount Rate Risk Oracle is the correct implementation with the correct config on all chains.
The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.