# Proposal 48. add Flash borrowers.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=48](https://vote.onaave.com/proposal/?proposalId=48)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-add-contango-protocol-cian-protocol-and-index-coop-to-flashborrowers-on-aave-v3/16478](https://governance.aave.com/t/arfc-add-contango-protocol-cian-protocol-and-index-coop-to-flashborrowers-on-aave-v3/16478)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x8853c5213ed32cc312c4577fed8AB1BA97CE3F8D#code#F1#L1)

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0xE7F84fb0E329aBd1d06Bdc576F14Cff00eFA4A66#code#F1#L1)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x2D007603d02d7ab8E58FBBf89d46a8F9c50D1aa7#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:handshake: permission granting or revoking

<br>

### Context

This proposal sets various teams to be Flashborrowers of Aave V3 on Ethereum, Arbitrum, and Optimism liquidity pools. The below summaries each initiative:
- Ethereum:
    Index Coop, Cian Protocol, Contango Protocol, Aave-Aligned protocol.

- Optimism:
    Contango.

- Arbitrum:
    Contango.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x749f063ce435b737df50439f3c5dd3081a54eefd6d2037337fa6b763159706b6](https://etherscan.io/tx/0x749f063ce435b737df50439f3c5dd3081a54eefd6d2037337fa6b763159706b6)

```
- proposalId: 48
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x925b92bc979665e02c8d91956e8c01dd9e5e4b9fbb3e2c5ab018b4a6a91e6d00
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
      "payloadId": "78" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "16" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "14" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x925b92bc979665e02c8d91956e8c01dd9e5e4b9fbb3e2c5ab018b4a6a91e6d00" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/48.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/48.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/78.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/78.md)

* Optimism - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/16.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/16.md)

* Arbitrum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/14.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/14.md)

<br>

### Technical analysis

We have verified that the payloads sets the following contracts as flash borrowers on the following chains:
- the addresses on Ethereum:
    0x45c00508C14601fd1C1e296eB3C0e3eEEdCa45D0 (Index Coop).

    0x6e8ac99B2ec2e08600c7d0Aab970f31e9b11957a (Index Coop).

    0x3a657Ec8a755d2E43DDbfDeaDc15899EDaf8dcf8 (Index Coop).

    0x85105b7E11c442Ca6fF6b4d90d7a439f68376Ac4 (Cian Protocol).

    0xab515542d621574f9b5212d50593cD0C07e641bD (Contango Protocol).

    0xb5b29320d2Dde5BA5BAFA1EbcD270052070483ec (Aave-Aligned protocol).

    0x0274a704a6D9129F90A62dDC6f6024b33EcDad36 (Aave-Aligned protocol).

- the address on Arbitrum:
    0x5e2aDC1F256f990D73a69875E06AF8A8404e3a03 (Contango Protocol).

- the address on Optimism:
    0xab515542d621574f9b5212d50593cD0C07e641bD (Contango Protocol).

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
