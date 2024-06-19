# Proposal 120. GHO Cross-Chain - Part 1.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=120](https://vote.onaave.com/proposal/?proposalId=120)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-gho-cross-chain-launch/17616](https://governance.aave.com/t/arfc-gho-cross-chain-launch/17616)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xa6D18e52ACc597de5E58e47586E6a3984B1Af749#code#F1#L1)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0xD2C06Cabc9E9734ECE5fBA04717346298eaa893f#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:scroll::small_red_triangle: contract upgrade

:handshake: permission granting or revoking

<br>

### Context

This proposal is the first part of the the GHO-Cross-Chain plan which is the implementation of GHO stablecoin, beginning with the initial expansion to the Arbitrum network utilizing the Chainlink Cross-Chain Interoperability Protocol (CCIP). The second step will onboard GHO on Arbitrum-v3.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x98230f63b5f2fbd05a457ae722298aa3a669659e9375d1aa60c5b3f993cc84c3](https://etherscan.io/tx/0x98230f63b5f2fbd05a457ae722298aa3a669659e9375d1aa60c5b3f993cc84c3)

```
- proposalId: 120
- creator: 0x66a28531e6f390a8cd44ab0c57a0f1aeb7e673ff
- accessLevel: 1
- ipfsHash: 0x6bfacf65a23e1f55bb84672797c83aa265f061be5a27f55f74d6fa34cd63b300
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
      "payloadId": "137" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "32" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x6bfacf65a23e1f55bb84672797c83aa265f061be5a27f55f74d6fa34cd63b300" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/120.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/120.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/137.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/137.md)

* Arbitrum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/32.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/32.md)

<br>

### Technical analysis

We have verified that the payload is doing the following actions:

**Ethereum**

* Deployment of CCIP LockReleaseTokenPool Contract on Ethereum.

* Transfer of ownership of the CCIP LockReleaseTokenPool contract to the DAO on Ethereum

* Configuration of CCIP LockReleaseTokenPool contract on Ethereum.

**Arbitrum**

* Deployment of UpgradeableGHO Contract on Arbitrum.

* Deployment of BurnMintTokenPool Contract on Arbitrum.

* Transfer of ownership of the CCIP BurnMintTokenPool contract to the DAO on Arbitrum.

* Configuration of CCIP BurnMintTokenPool contract on Arbitrum.



<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
