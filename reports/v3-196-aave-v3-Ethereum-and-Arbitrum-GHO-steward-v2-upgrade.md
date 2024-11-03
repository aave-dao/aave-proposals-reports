# Proposal 196. GHO Steward v2 Upgrade

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=196](https://vote.onaave.com/proposal/?proposalId=196)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-gho-steward-v2-upgrade/19116](https://governance.aave.com/t/arfc-gho-steward-v2-upgrade/19116)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x18F74428230cB84c6FFF694614a453b9cE5aeb20#code)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x3C916e95C3E882daBD983396D27d0a2AC1fBdf7e#code)

<br>

## Certora analysis

<br>

### Proposal types

:handshake: permission granting or revoking

<br>

### Context

This proposal seeks to upgrade the GHO Steward role in the Aave ecosystem to accommodate the growing needs of GHO, Aave’s native decentralized stablecoin. By introducing specialized stewards—GhoBucketSteward, GhoAaveSteward, GhoCcipSteward, and GhoGsmSteward—the proposal aims to streamline governance, delegate specific responsibilities, and enhance scalability for future developments of GHO.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x1f32c0b7c559b62b5f7640ac1002de08bbf524fe88bb55f02c673d2ad5ec914d](https://etherscan.io/tx/0x1f32c0b7c559b62b5f7640ac1002de08bbf524fe88bb55f02c673d2ad5ec914d)

```
- proposalId: 196
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xf537d68c6b1b19b3fc6dc6ed5b73e2479fb8daabac2e275ebb787012a353455d
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "1", 
      "accessLevel": "1", 
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5", 
      "payloadId": "202" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "58" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xf537d68c6b1b19b3fc6dc6ed5b73e2479fb8daabac2e275ebb787012a353455d" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/196.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/196.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/202.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/202.md)

* Arbitrum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/58.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/58.md)

<br>

### Technical analysis

We have verified that the payload upgrades the GHO Steward role by introducing the specialized stewards as outlined in the IPFS. The new stewards—GhoBucketSteward, GhoAaveSteward, GhoCcipSteward, and GhoGsmSteward—have been granted the appropriate roles and permissions within the Aave protocol. The payload correctly revokes roles from the old steward and assigns them to the new stewards, ensuring a seamless transition. Additionally, the new CCIP Token Pool on Arbitrum has been deployed and upgraded as specified, allowing the setting of the RateLimitAdmin. Overall, the technical implementation aligns with the proposal’s objectives and has been executed correctly.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

