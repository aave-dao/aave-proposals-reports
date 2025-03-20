# Proposal 270. Clinic steward activation

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=270)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-bgd-aave-clinicsteward/21209)

### Payloads

* Ethereum Core - [proposal payloads](https://etherscan.io/address/0x4caB0c8deb2A116332c1f8584590aA7Bd79eC0FC)

* Ethereum Prime - [proposal payloads](https://etherscan.io/address/0x2990d304c53A257dC0dd15Ac25c8558D7F4C7fA9)

* Polygon - [proposal payloads](https://polygonscan.com/address/0xE45acDC3e8C1d9Db5968b23c636DA0929f64d2A4)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xc3917d67323A7F2933D1F0326507C2815E31030F)

* OP Mainnet - [proposal payloads](https://optimistic.etherscan.io/address/0x69013B05324010b89486a1193Cd9Ed9cF2f568c3)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0xE02ee81872F20C7052821B7389fd3e2eb9c99847)

* Metis - [proposal payloads](https://explorer.metis.io/address/0x2a10c034F3A4301985a9058aA09dE64a9Cc6d8E7)

* Base - [proposal payloads](https://basescan.org/address/0xbC0349a958C1A7f098C4966bb480fD15Ba8eA5C1)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0xCf132F9a344cE1b222d594F1D520638AA8DF96b6)

* Scroll - [proposal payloads](https://scrollscan.com/address/0xFEc5ebF148e91a6090F5b1657eddF31b85dcE74e)

* BNB Smart Chain - [proposal payloads](https://bscscan.com/address/0x9FF867B7De93cf504AC8a752ccE3044b3F2b5816)

* zkSync Era - [proposal payloads](https://era.zksync.network/address/0xEdBb23D39128d0009980416DDe9139623f7A0171)

* Linea - [proposal payloads](https://lineascan.build//0xE003e128d53D1A290756900cF06ED1efBa5f6B9F)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking

### Context
Enabling a new Aave ClinicSteward smart contract, with capabilities to liquidate and repay non-healthy positions. The contract will utilize Aave Collector funds for the repayment.

### Proposal Creation
Transaction: [0x1addfea1e453c180aee44eba16185427f557894c113f0f5fa730dfce6f587253](https://etherscan.io/tx/0x1addfea1e453c180aee44eba16185427f557894c113f0f5fa730dfce6f587253)
- `proposalId`: 270
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x4043001b72316afa6b6728772941bfa08f127b66c1c006316a3f20510b6738ab

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 256,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 104,
        },
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 71,
        },
        {
            chain: "10",
            payloads_controller: "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
            payload_id: 69,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 78,
        },
        {
            chain: "1088",
            payloads_controller: "0x2233F8A66A728FBa6E1dC95570B25360D07D5524",
            payload_id: 35,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 60,
        },
        {
            chain: "100",
            payloads_controller: "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
            payload_id: 46,
        },
        {
            chain: "534352",
            payloads_controller: "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE",
            payload_id: 36,
        },
        {
            chain: "56",
            payloads_controller: "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627",
            payload_id: 34,
        },
        {
            chain: "324",
            payloads_controller: "0x2E79349c3F5e4751E87b966812C9E65E805996F1",
            payload_id: 18,
        },
        {
            chain: "59144",
            payloads_controller: "0x3BcE23a1363728091bc57A58a226CF2940C2e074",
            payload_id: 5,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0x4043001b72316afa6b6728772941bfa08f127b66c1c006316a3f20510b6738ab",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/270.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/256.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/104.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/71.md)

* OP Mainnet - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/69.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/78.md)

* Metis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/35.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/60.md)

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/46.md)

* Scroll - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/36.md)

* BNB Smart Chain - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/34.md)

* zkSync Era - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/324/0x2E79349c3F5e4751E87b966812C9E65E805996F1/18.md)

* Linea - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/59144/0x3BcE23a1363728091bc57A58a226CF2940C2e074/5.md)


### Technical Analysis
We made a comprehensive audit on the steward and shared a report with our findings which were fixed. We have verified the specified caps were implemented correctly on every chain and the correct version of the steward was uploaded.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.