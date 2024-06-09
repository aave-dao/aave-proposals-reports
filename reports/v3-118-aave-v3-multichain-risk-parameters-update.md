# Proposal 118. Risk Parameter Updates AaveV3.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=118](https://vote.onaave.com/proposal/?proposalId=118)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-aave-v3-05-24-2024/17788](https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-aave-v3-05-24-2024/17788)

<br>

### Payloads

* Polygon - [proposal payloads](https://polygonscan.com/address/0xDF188c8d176Bc3549e9A53005FF8BCc68Eef22A3#code#F1#L1)

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0xd41DE48545494C57A682EF4cdb0e960E19303bb9#code#F1#L1)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x348dF1A44E6B862434714e9A45A1cd88Cb0e670c#code#F1#L1)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x88CFACDe9c3684AB205567B8228cD49D460Fe4A7#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal suggests interest rate parameters changes to the native tokens across 4 different chains to create greater capital efficiency.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xea70d189ce7ad99f79b5f4044c7780dd434085d74b953527732895ea7f73292e](https://etherscan.io/tx/0xea70d189ce7ad99f79b5f4044c7780dd434085d74b953527732895ea7f73292e)

```
- proposalId: 118
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x0f87c9e8fca1a544a44d37f7d5d0b37d7fbf86f4d8b30695090b077b81bb7cb8
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "67" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "34" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "31" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "20" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x0f87c9e8fca1a544a44d37f7d5d0b37d7fbf86f4d8b30695090b077b81bb7cb8" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/118.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/118.md)

**Payload reports**

* Polygon V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/67.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/67.md)

* Optimism V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/34.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/34.md)

* Arbitrum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/31.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/31.md)

* Gnosis V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/20.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/20.md)

<br>

### Technical analysis

We have verified that the payloads modify the LTV and LT of the following assets to the declared values:

- stMatic - LTV = 48%, LT = 58%

- MaticX - LTV = 50%, LT = 60%

- OP - LTV = 58%, LT = 63%

- ARB - LTV = 58%, LT = 63%

- GNO - LTV = 48%, LT = 53%

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
