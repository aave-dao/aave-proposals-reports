# Proposal 483. Add CoW Swap Adapters to flashBorrowers

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=483)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-whitelist-cow-protocol-adapters-as-flash-borrowers-on-aave-v3/24467)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x50Af4f6eCb2014EcE52d0Bf35e4847F6ACc16c11)

* Polygon - [proposal payloads](https://polygonscan.com/address/0xB9490Aa7eB0644CEABdAB97be3b23e0be2EEed3D)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xB9490Aa7eB0644CEABdAB97be3b23e0be2EEed3D)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0xB9490Aa7eB0644CEABdAB97be3b23e0be2EEed3D)

* Base - [proposal payloads](https://basescan.org/address/0xb8C388282851DB2c96D30634fC8Af439091eeabc)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x9cc7BE24a758F9184DC846eB2A99ACc2B5390B0E)

* BNB Smart Chain - [proposal payloads](https://bscscan.com/address/0x813084eAB9F79a54139BF0e37D0F518EFfC7889c)

* Linea - [proposal payloads](https://lineascan.build/address/0xF29CBcA0eaE94A4471A604846E8EfcB39C1A2fB8)

* Plasma - [proposal payloads](https://plasmascan.to/address/0x446da28203bbd6be2f1237f994d49d8c428eec5a)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking

### Context
This proposal seeks to register Aave Swap Adapter factories as approved flash borrowers across relevant Aave V3 instances, enabling them to access flash liquidity with zero flash loan fees.

This change improves execution quality for users interacting through Aave’s swap flows by removing an internal protocol fee that currently adds avoidable cost to adapter-based routing.

### Proposal Creation
Transaction: [0x717ced8b5fa3085e52da1000def40f329be42d8818b2406cad360530647eaf85](https://etherscan.io/tx/0x717ced8b5fa3085e52da1000def40f329be42d8818b2406cad360530647eaf85)
- `proposalId`: 483
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0xc96375d0b7a0d7daa767f0c64c420e1a2e27b36baa56ad8b850d1e91ceba2504

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 436,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 143,
        },
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 114,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 127,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 107,
        },
        {
            chain: "100",
            payloads_controller: "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
            payload_id: 75,
        },
        {
            chain: "56",
            payloads_controller: "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627",
            payload_id: 58,
        },
        {
            chain: "59144",
            payloads_controller: "0x3BcE23a1363728091bc57A58a226CF2940C2e074",
            payload_id: 26,
        },
        {
            chain: "9745",
            payloads_controller: "0xe76EB348E65eF163d85ce282125FF5a7F5712A1d",
            payload_id: 26,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xc96375d0b7a0d7daa767f0c64c420e1a2e27b36baa56ad8b850d1e91ceba2504",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/483.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/436.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/143.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/114.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/127.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/107.md)

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/75.md)

* BNB Smart Chain - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/58.md)

* Linea - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/59144/0x3BcE23a1363728091bc57A58a226CF2940C2e074/26.md)

* Plasma - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/26.md)


### Technical Analysis

We have verified that the proposal grants the Aave V3 `FLASH_BORROWER` role (`0x939b8dfb57ecef2aea54a93a15e86768b9d4089f1ba61c245e6ec980695f4ca4` = `keccak256("FLASH_BORROWER")`) to the CoW Protocol address `0xdeCC46a4b09162F5369c5C80383AAa9159bCf192` on every targeted instance's `ACLManager`, enabling 0-premium flash-borrowing for CoW Swap settlement.

The same role grant is performed independently on each of the nine chains: Ethereum, Polygon, Avalanche, Arbitrum, Base, Gnosis, BNB Smart Chain, Linea, and Plasma. No other state is mutated by any of the payloads — no reserve parameters, no transfers, and no other role changes.

We have verified the payload's logic and validated its execution via Seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.