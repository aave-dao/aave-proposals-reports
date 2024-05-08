# Proposal 100. Generalized LT/LTV Reductions on Aave V3 Step 2.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=100](https://vote.onaave.com/proposal/?proposalId=100)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-generalized-lt-ltv-reductions-on-aave-v3-step-2-04-23-2024/17455](https://governance.aave.com/t/arfc-generalized-lt-ltv-reductions-on-aave-v3-step-2-04-23-2024/17455)

<br>

### Payloads

* Ethereum V3- [proposal payloads](https://etherscan.io/address/0x7F9Cc7079Ab0c2AFc4613ce30653870C92245e54#code#F1#L1)

* Polygon V3- [proposal payloads](https://polygonscan.com/address/0x2BE5253e2D8CE8487efD6a21B5e63fB8D5c76B3c#code#F1#L1)

* Avalanche V3- [proposal payloads](https://snowscan.xyz/address/0x695133dD0F01D745E78e97b1CFECE73484A696ca#code#F1#L1)

* Optimism V3- [proposal payloads](https://optimistic.etherscan.io/address/0x7B55BdBaDe8B990B1cA58d6b7B1F856e4d66a03F#code#F1#L1)

* Arbitrum V3- [proposal payloads](https://arbiscan.io/address/0xEc3002522ec65722a1e74C9137bFEAa36295436d#code#F1#L1)

* Base V3- [proposal payloads](https://basescan.org/address/0x4aA5328ac7eA2c8652Ba9d2Cb70C56532bA683d9#code#F1#L1)

* Gnosis V3- [proposal payloads](https://gnosisscan.io/address/0xfe32dd387e4922Bc2c53cf4b51080B41BA8d5610#code#F1#L1)

* Scroll V3- [proposal payloads](https://scrollscan.com/address/0xd947dd3190Eac399DADF47983B3DB12aAd543348#code#F1#L1)

* BNB V3- [proposal payloads](https://bscscan.com/address/0xdBBD13b9F9c6CEbab42d2054eEd5722D5a2940e6#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal adjusts the LTs and LTVs of multiple stable-coins on Aave-V3 markets to 75% and 78% in response to the volatility risks highlighted by the UNI incident on Compound.

Note that for USDC.e on Optimism, the LT will be 80% and that for USDC on Avalanche, the LT will be 81%.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xb45582da92bbd8b471871655b15142482e9233ef5edabd88f57ffe82287f43b2](https://etherscan.io/tx/0xb45582da92bbd8b471871655b15142482e9233ef5edabd88f57ffe82287f43b2)

```
- proposalId: 100
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x662b22b8e2ddeeb5f0b9f85cc16f8dfb2e1c8fa5d0d2f646773e9709eb02dcff
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
      "payloadId": "122" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "61" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "32" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "30" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "28" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "19" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "18" 
    }, 
    { 
      "chain": "534352", 
      "accessLevel": "1", 
      "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE", 
      "payloadId": "12" 
    }, 
    { 
      "chain": "56", 
      "accessLevel": "1", 
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627", 
      "payloadId": "14" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x662b22b8e2ddeeb5f0b9f85cc16f8dfb2e1c8fa5d0d2f646773e9709eb02dcff" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/100.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/100.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/122.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/122.md)

* Polygon - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/61.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/61.md)

* Avalanche - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/32.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/32.md)

* Optimism - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/30.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/30.md)

* Arbitrum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/28.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/28.md)

* Base - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/19.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/19.md)

* Gnosis - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/18.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/18.md)

* Scroll - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/12_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/12_forge.md)

* BNB - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/14.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/14.md)

<br>

### Technical analysis

We have verified that the payload modifies the LTs and LTVs of the following tokens to the following values on the following platforms:

- Ethereum:

    USDC: LT: 75%, LTV: 78%

    USDT: LT: 75%, LTV: 78%

    sDAI: LT: 75%, LTV: 78%

- Polygon:

    USDC: LT: 75%, LTV: 78%

    USDT: LT: 75%, LTV: 78%

    USDC.e: LT: 75%, LTV: 78%

- Avalanche:

    USDC: LT: 75%, LTV: 81%

- Optimism:

    USDC: LT: 75%, LTV: 78%

    USDT: LT: 75%, LTV: 78%

    USDC.e: LT: 75%, LTV: 80%

- Arbitrum:

    USDC: LT: 75%, LTV: 78%

    USDT: LT: 75%, LTV: 78%

    USDC.e: LT: 75%, LTV: 78%

- Base:

    USDC: LT: 75%, LTV: 78%

    USDbC: LT: 75%, LTV: 78%

- Gnosis:

    USDC: LT: 75%, LTV: 78%

    sDAI: LT: 75%, LTV: 78%

- Scroll:

    USDC: LT: 75%, LTV: 78%

- BNB:

    USDC: LT: 75%, LTV: 78%

    USDT: LT: 75%, LTV: 78%

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
