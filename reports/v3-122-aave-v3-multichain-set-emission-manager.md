# Proposal 122. Set ACI as Emission Manager for Aave Liquidity Mining programs.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=122](https://vote.onaave.com/proposal/?proposalId=122)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-set-aci-as-emission-manager-for-liquidity-mining-programs/17898](https://governance.aave.com/t/arfc-set-aci-as-emission-manager-for-liquidity-mining-programs/17898)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xBb615C054A50D73aA60F1C5b9aB1Ffc0CD03c506#code#F1#L17)

* Avalanche - [proposal payloads](https://arbiscan.io/address/0x443Cf2c974c5b63f8173296431207996010841D9#code#F1#L22)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal sets ACI multisig as the emission manager of ARB and SD in order to distribute rewards to users, which will incentivize more engagement with the protocol.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x2937898c33616327b66cd0f57bf679e821de688c7b440fe6f6de6556983b79ce](https://etherscan.io/tx/0x2937898c33616327b66cd0f57bf679e821de688c7b440fe6f6de6556983b79ce)

```
- proposalId: 122
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xc3fb70a23e9e6e2654fb3119fe3315859e590f3f9115ee56a3b22c68804da75d
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
      "payloadId": "139" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "34" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xc3fb70a23e9e6e2654fb3119fe3315859e590f3f9115ee56a3b22c68804da75d" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/122.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/122.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/139.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/139.md)

* Arbitrum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/34.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/34.md)

<br>

### Technical analysis

We have verified that the ACI multisig address was set to be the emission manager of ARB on Arbitrum and SD on Ethereum.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
