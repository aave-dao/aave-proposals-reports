# Proposal 481. Complete Offboarding Plan for Chaos Labs

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=481)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/orderly-transition-and-offboarding-plan-for-chaos-labs/24399)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xDaF2A2a63DA5dd1e0dcafA4f43398b41f81AE941)

* Plasma - [proposal payloads](https://plasmascan.to/address/0x76ef87d9c9804e9f5ec8fb24f1f1cb6ab7dd4da9)



## Certora Analysis

### Proposal Types

* :moneybag: :receipt: Asset transfers
* :handshake: Permission granting and revoking
* :bank: Payment stream

### Context
This proposal submits a follow-up payload to complete the AgentHub offboarding actions associated with AIP-479.

The payload removes the remaining Agent permissions on Ethereum mainnet and removes the corresponding AgentHub permissions on Plasma. No new permissions are granted and no market configuration is changed.


### Proposal Creation
Transaction: [0xb8bdd5a7a0b4a7f24f284c3f3777361a12fbd5097f9e1c1b0dafee9a45278e0d](https://etherscan.io/tx/0xb8bdd5a7a0b4a7f24f284c3f3777361a12fbd5097f9e1c1b0dafee9a45278e0d)
- `proposalId`: 481
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0xdb9ebeac9b9f3da123536227af6e3fb227da0e4c16e4adc2a8dba66d0f5ef777

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 434,
        },
        {
            chain: "9745",
            payloads_controller: "0xe76EB348E65eF163d85ce282125FF5a7F5712A1d",
            payload_id: 25,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xdb9ebeac9b9f3da123536227af6e3fb227da0e4c16e4adc2a8dba66d0f5ef777",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/481.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/434.md)

* Plasma - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/25.md)


### Technical Analysis

We have verified that the proposal completes the Chaos Labs offboarding on Aave V3 Ethereum and Aave V3 Plasma:

* Aave V3 Ethereum (payload action contract `0xDaF2A2a63DA5dd1e0dcafA4f43398b41f81AE941`): revokes the `RISK_ADMIN` role (`0x8aa855a911518ecfbe5bc3088c8f3dda7badf130faaf8ace33fdc33828e18167`) from 4 addresses on the Aave V3 Ethereum Core `ACLManager` (`0xc2aaCf6553D20d1e9d78E365AAba8032af9c85b0`) - `0x4F2858d4A4e4464b34Aa4a22C41B2Ef540a59BF4`, `0x1B3bD355c43d2247946b8e0889d4b4e701bf430d`, `0xdA626E64f34f24e0236E0C9cD2F11ce4549a08c6`, `0xCc18Be380838956aad41FD22466085eD66aaBB46` - and from 2 addresses on the Aave V3 Ethereum Lido `ACLManager` (`0x013E2C7567b6231e865BB9273F8c7656103611c0`) - `0x52E652182b22C41d0202bB8D834982F43B12Cd21`, `0xCc18Be380838956aad41FD22466085eD66aaBB46`. The payload additionally cancels stream `100073` on the Aave Collector (`0x464C71f6c2F760DdA6093dCB91C24c39e5d6e18c`), transferring the vested aGHO (~243,627.85 GHO plus ~206.12 GHO minted accrual) to the stream recipient `0xbC540e0729B732fb14afA240aA5A047aE9ba7dF0`.

* Aave V3 Plasma (payload action contract `0x76ef87d9c9804e9f5ec8fb24f1f1cb6ab7dd4da9`): revokes the `RISK_ADMIN` role from `0x3999d49Bbad3A7375B0376BDF2bA4f2e3c9F5177` and `0x4e8984D11A47Ff89CD67c7651eCaB6C00a74B4A9` on the Plasma `ACLManager` (`0xa860355F0ccFdC823F7332ac108317b2a1509C06`), and disables both Chaos Labs agents in the `AgentHub`.

We have verified that no other state is mutated by the payloads.

We have verified the payload's logic and validated its execution via Seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.