# Proposal 271. Stablecoins Interest Rate Curve Update

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=271)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-stablecoin-interest-rate-curve-update-03-04-2025/21269)

### Payloads

* Ethereum Core - [proposal payloads](https://etherscan.io/address/0x50fbD9C93fbF99C38104b1dcAe84cE0d2071b440)

* Ethereum Prime - [proposal payloads](https://etherscan.io/address/0xAf54Cd5e62b995059C1ef507B7de67d403b42ed4)

* Ethereum Ether.Fi - [proposal payloads](https://etherscan.io/address/0x89B6d89fb3cFE5c59cb7d972c4DDb81aFC160272)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xb7A82d685677A0085f96815a0DC4521BFDFA7156)

* OP Mainnet - [proposal payloads](https://optimistic.etherscan.io/address/0xB553Cf1d27C2595524f837F0a8C8736a0Ae70F5F)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0x73e117f3D7F02a2e69E851203eBcdFfacb6263CD)

* Metis - [proposal payloads](https://explorer.metis.io/address/0x6668e20492dbBa0494019C9D333BeE456928520B)

* Base - [proposal payloads](https://basescan.org/address/0xBda7dF5939B5eD34e52E71678A16A39db506b475)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x1Fc0450B42cd137e4fFc06b7b8c102D246Af2a6d)

* Scroll - [proposal payloads](https://scrollscan.com/address/0x65dAc98e5D04547d7E5ac994eabeA0322936F7ba)

* BNB Smart Chain - [proposal payloads](https://bscscan.com/address/0xE38C9AC9f167deAa8DB30b98a2C5E109c88CBb00)

* zkSync Era - [proposal payloads](https://era.zksync.network/address/0xeD995f040Ba5c606D6945400a29087dB35209314)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
Setting the target borrow rate for most stablecoins to 6.50%. These changes would be implemented via the direct-to-AIP process.
### Proposal Creation
Transaction: [0xebbd35661fa3324b49b42c0ba937c15afddd6e4b98600fd63cd3786177aa1c10](https://etherscan.io/tx/0xebbd35661fa3324b49b42c0ba937c15afddd6e4b98600fd63cd3786177aa1c10)
- `proposalId`: 271
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xd1c8efdc310bd2fdd2d4f00fdeb9c01758078f56d24218c778d58132f11f1104

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 259,
        },
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 72,
        },
        {
            chain: "10",
            payloads_controller: "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
            payload_id: 70,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 80,
        },
        {
            chain: "1088",
            payloads_controller: "0x2233F8A66A728FBa6E1dC95570B25360D07D5524",
            payload_id: 36,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 62,
        },
        {
            chain: "100",
            payloads_controller: "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
            payload_id: 47,
        },
        {
            chain: "534352",
            payloads_controller: "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE",
            payload_id: 37,
        },
        {
            chain: "56",
            payloads_controller: "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627",
            payload_id: 35,
        },
        {
            chain: "324",
            payloads_controller: "0x2E79349c3F5e4751E87b966812C9E65E805996F1",
            payload_id: 19,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0xd1c8efdc310bd2fdd2d4f00fdeb9c01758078f56d24218c778d58132f11f1104",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/271.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/259.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/72.md)

* OP Mainnet - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/70.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/80.md)

* Metis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/36.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/62.md)

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/47.md)

* Scroll - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/37.md)

* BNB Smart Chain - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/35.md)

* zkSync Era - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/324/0x2E79349c3F5e4751E87b966812C9E65E805996F1/19.md)


### Technical Analysis
We have verified the specified assets were modified to 6.5% with right decimal precision. 

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.