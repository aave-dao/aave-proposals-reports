# Proposal 478. rsETH Incident: Liquidate rsETH attacker positions

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=478)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/rseth-incident-report-april-20-2026/24580)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x0cD3138eFF780D1e6e6c2e3CD72405246861053c)

* Ethereum - [proposal payloads](https://etherscan.io/address/0x43EE256b82AC62A6B6b94Ae56dADF2c21cBCA12e)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0xD9e90016cF3Fd38475A4689eC1978A495638de3A)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0xbc298839a9d6b42A85Bba36fD6F61a378C55A9E0)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0x95BD57c3726e6bA8668A877D7b4afFfDF9C90D68)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0xE48362cd9182d92E6445119655961cD25cdA26Df)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0xdA946475eA9CE0C3a93d87D08281fdFEB968079c)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0xa179B31E7092Ee9E0109e79Fb2A6876102CEc795)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates
* :gem: :new: Listing new assets


### Context
As part of the Defi United recovery effort and technical plan, this proposal executes liquidations against the identified rsETH attacker’s positions on Aave V3 Ethereum Core and Aave V3 Arbitrum, subject to each position being eligible for liquidation at execution time.

The proposal is intended to reduce outstanding bad debt risk, recover available rsETH collateral through normal Aave liquidation mechanics, and route any recovered value according to the DAO-approved rsETH incident recovery process.

### Proposal Creation
Transaction: [0xefec6b0738eab724c9095c009fd7f922f78908f9ea62f3078789b3399dd2c954](https://etherscan.io/tx/0xefec6b0738eab724c9095c009fd7f922f78908f9ea62f3078789b3399dd2c954)
- `proposalId`: 478
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0x73d6b6ffb8c006af7464dc28e66df897bea1b011662efaa209c7503736612881

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 431,
        },
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 432,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 121,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 122,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 123,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 124,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 125,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 126,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x73d6b6ffb8c006af7464dc28e66df897bea1b011662efaa209c7503736612881",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/478.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/431.md)

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/432.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/121.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/122.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/123.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/124.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/125.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/126.md)


### Technical Analysis

We have verified that the proposal consists of eight single-action liquidation payloads - two on Aave V3 Ethereum Core and six on Aave V3 Arbitrum - corresponding 1:1 to the eight attacker positions documented in the published rsETH incident report. Each payload's `execute()` delegates to a dedicated liquidation contract that invokes `Pool.liquidationCall` against a single attacker position with rsETH as the collateral asset, targeting the following wallets identified in the report:

* Aave V3 Ethereum Core: `0x1f4c1c2e610f089d6914c4448e6f21cb0db3adef`, `0x8d11aeac74267dd5c56d371bf4ae1afa174c2d49`.
* Aave V3 Arbitrum: `0xeba786c9517a4823a5cfd9c72e4e80bf8168129b`, `0xcbb24a6b4dafaaa1a759a2f413ea0eb6ae1455cc`, `0x1b748b680373a1dd70a2319261328cab2a6f644c`, `0xbb6a6006eb71205e977eceb19fcad1c8d631c787`, `0xe9e2f48bb0018276391aec240abb46e8c3cad181`, plus `0x8d11aeac74267dd5c56d371bf4ae1afa174c2d49` (the wallet appearing on both chains).

We have verified that each payload is permissioned at `accessLevel: 1`, performs a single delegatecall, and mutates no other state beyond the liquidation flow.

We have verified the payload's logic and validated its execution via Seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.