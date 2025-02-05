# Proposal 239. Collector upgrade

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=239)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/technical-maintenance-proposals/15274/63)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xb65B0ed60365283C81b91b4BbA694BD71b8F90ce)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x487c2C53c0866F0A73ae317bD1A28F63ADcD9aD1)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xd76eCc4426482650d26927148F67E0C59ce8F0D6)

* OP Mainnet - [proposal payloads](https://optimistic.etherscan.io/address/0x29200edbE4653d49AFe0A8a213A3A93137919530)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x4Daf1ad67CB9eEb004c338330e09d02125Fb371D)

* Metis - [proposal payloads](https://explorer.metis.io/address/0x0c2C95b24529664fE55D4437D7A31175CFE6c4f7)

* Base - [proposal payloads](https://basescan.org/address/0x209Ad99bd808221293d03827B86cC544bcA0023b)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x5E76E98E0963EcDC6A065d1435F84065b7523f39)

* Scroll - [proposal payloads](https://scrollscan.com/address/0xd9Ca4878dd38B021583c1B669905592EAe76E044)

* BNB Smart Chain - [proposal payloads](https://bscscan.com/address/0xd9Ca4878dd38B021583c1B669905592EAe76E044)

* zkSync - [proposal payloads](https://era.zksync.network/address/0xa5569DA53e95dD6311f01CCE03FA0BAD56d04125)

* Linea - [proposal payloads](https://lineascan.build//0xd1B3E25fD7C8AE7CADDC6F71b461b79CD4ddcFa3)



## Certora Analysis

### Proposal Types

* :scroll: :small_red_triangle: Contract upgrades

### Context
This proposal will upgrade the Aave Collector across all networks, to allow **multiple** funds admins.

This is a resubmission of [Proposal 237](https://vote.onaave.com/proposal/?proposalId=237&ipfsHash=0xa79bea5c305b0e5fb9a32e403c0d647db3278e46a0f302f94b0f172cb6060e98), which was [cancelled](https://governance.aave.com/t/technical-maintenance-proposals/15274/67) due to a detected inconsistency between networks.

### Proposal Creation
Transaction: [0x5d5109bbb580bd0369c30b2ded370a04d48b066c2c487838614910758f6ac8f9](https://etherscan.io/tx/0x5d5109bbb580bd0369c30b2ded370a04d48b066c2c487838614910758f6ac8f9)
- `proposalId`: 239
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x2e01049c4230c97d5d79d717a2753584e0bf3624c2364ef19ba32f14189cc0c1

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 239,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 95,
        },
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 65,
        },
        {
            chain: "10",
            payloads_controller: "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
            payload_id: 63,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 70,
        },
        {
            chain: "1088",
            payloads_controller: "0x2233F8A66A728FBa6E1dC95570B25360D07D5524",
            payload_id: 32,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 51,
        },
        {
            chain: "100",
            payloads_controller: "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
            payload_id: 42,
        },
        {
            chain: "534352",
            payloads_controller: "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE",
            payload_id: 32,
        },
        {
            chain: "56",
            payloads_controller: "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627",
            payload_id: 31,
        },
        {
            chain: "324",
            payloads_controller: "0x2E79349c3F5e4751E87b966812C9E65E805996F1",
            payload_id: 12,
        },
        {
            chain: "59144",
            payloads_controller: "0x3BcE23a1363728091bc57A58a226CF2940C2e074",
            payload_id: 1,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0x2e01049c4230c97d5d79d717a2753584e0bf3624c2364ef19ba32f14189cc0c1",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/239.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/239.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/95.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/65.md)

* OP Mainnet - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/63.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/70.md)

* Metis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/32.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/51.md)

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/42.md)

* Scroll - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/32.md)

* BNB Smart Chain - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/31.md)

* zkSync - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/324/0x2E79349c3F5e4751E87b966812C9E65E805996F1/12.md)

* Linea - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/59144/0x3BcE23a1363728091bc57A58a226CF2940C2e074/1.md)


### Technical Analysis
We have reviewed the changes to the collector prior to deployment and submitted our findings in a report. Moreover, after the discovery of the missing receive() payable function, we conducted the necessary checks to ensure the collector was uploaded correctly and that there are no other problematic differences between the live collector and the upgraded one

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.