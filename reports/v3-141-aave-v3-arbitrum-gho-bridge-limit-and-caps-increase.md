# Proposal 141. GHO Arbitrum Parameter Adjustments.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=141](https://vote.onaave.com/proposal/?proposalId=141)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-gho-arbitrum-parameter-adjustments/18386](https://governance.aave.com/t/arfc-gho-arbitrum-parameter-adjustments/18386)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x9fd20e53072318Abbc89e57Ddb42f090224fe95D)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0xB7f8306B3810657DE680c6190246966D929cD61F)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal increases the cross-chain gho limit on arbitrum due to the success of prior increase, where the new cap was filled within 90 minutes.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x892721e2fe22d2beafca21995fec3df23bd388e47e9284d4a562ca0093e89698](https://etherscan.io/tx/0x892721e2fe22d2beafca21995fec3df23bd388e47e9284d4a562ca0093e89698)

```
- proposalId: 141
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x0ff75897749a65a504bb7f953f0d8c1e6f3eda9434fdf2959ff78909d4358589
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
      "payloadId": "152" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "41" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x0ff75897749a65a504bb7f953f0d8c1e6f3eda9434fdf2959ff78909d4358589" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/141.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/141.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/152.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/152.md)

* Arbitrum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/41.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/41.md)

<br>

### Technical analysis

We have verified that gho cap on arbitrum was increased to 20M.
This means:
1. The ccip gho bridge limit on Ethereum was increased to 20M.
2. The gho capacity of the ccip bridge on Arbitrum was raised to 20M.

In addition, we verified that the gho supply and borrow cap on the Arbitrum instance of Aave was changed to 5M and 4.5M respectively.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

