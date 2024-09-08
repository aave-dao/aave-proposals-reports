# Proposal 160. Reserve Factor & Slope1 Update.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=160](https://vote.onaave.com/proposal/?proposalId=160)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-increase-bridged-usdc-reserve-factor-across-all-deployments/17787](https://governance.aave.com/t/arfc-increase-bridged-usdc-reserve-factor-across-all-deployments/17787)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xaE1B4Eb6639Ef92c7f083F61040e95df98aAb0CE#code#F1#L1)
* Polygon V2 - [proposal payloads](https://polygonscan.com/address/0xDF266CC79F409186D073cABDbFCF136652A19d53#code#F1#L1)
* Polygon V3 - [proposal payloads](https://polygonscan.com/address/0xf89027372C7f1a186821B9ff8a998b8BeAEcC991#code#F1#L1)
* Avalanche - [proposal payloads](https://snowtrace.io/address/0xdDce535e5a25F237A085eb81020951870E669982/contract/43114/code)
* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0xDC2eC885bF5d9dE4D1E258F13bcA78b524cF8212#code#F1#L1)
* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x04F987Ed96Fa85d31CC78c9353D1668eb3FE85b4#code#F1#L1)
* Base - [proposal payloads](https://basescan.org/address/0xA7972711D0e4dee81B2a9ef31E13B77610Ac428B#code#F1#L1)
* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x9f964a4Be706dbd3DF1E8D54978cb314D0C1a5BB#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal sets new reserves factor across Aave deployments and sets slope1 parameter on Polygon assets.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xfd2f38e7c61e7d440199829796dd9a878fc96d24bf9738fbcbd4aa1cdc10a138](https://etherscan.io/tx/0xfd2f38e7c61e7d440199829796dd9a878fc96d24bf9738fbcbd4aa1cdc10a138)

```
- proposalId: 160
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xe77c05ca3ace3841039fbd4f73b81d8cbb98fde7e80724d0ae9d4f2f96f83348
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
      "payloadId": "168" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "81" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "52" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "47" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "49" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "34" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "30" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xe77c05ca3ace3841039fbd4f73b81d8cbb98fde7e80724d0ae9d4f2f96f83348" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/160.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/160.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/168.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/168.md)

* Polygon V2 + V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/81.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/81.md)

* Avalanche V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/52.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/52.md)

* Optimism V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/47.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/47.md)

* Arbitrum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/49.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/49.md)

* Base V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/34.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/34.md)

* Gnosis V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/30.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/30.md)


<br>

### Technical analysis

We have confirmed that the payload successfully adjusts the slope1 for the specified assets on Polygon and have also verified that it updates the reserve factor across Aave deployments.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
