# Proposal 173. Chaos Labs Risk Parameter Updates - LTV and LT Alignment.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=173](https://vote.onaave.com/proposal/?proposalId=173)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-ltv-and-lt-alignment/18997](https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-ltv-and-lt-alignment/18997)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x092B45033f494Bef3AF6a2594dD698e3fD39f246#code#F1#L1)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x37A87f3AF3D5108f95E98675687c9838EDa2Abbc#code#F1#L1)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x54a0bb225f1380E079FB531C08362179C2E7770d/contract/43114/code)

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0x0Caac2579CB7fA10Cc3BDCFF88c0F32fE5e6152c#code#F1#L1)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x87C0bd5e566b20Fc99E13785bC23C3cae4E4970f#code#F1#L1)

* Metis - [proposal payloads](https://explorer.metis.io/address/0x6444706925e7586e5B77CC0b9183b1FBfA053aA4/contract/1088/code)

* Base - [proposal payloads](https://basescan.org/address/0x8cc2AE80932B7D925165F646Dea3716B8b9CE30c#code#F1#L1)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0xE940d42751903FdE92090CdC400Ee45985a62230#code#F1#L1)

* Scroll - [proposal payloads](https://scrollscan.com/address/0x0a883C56e4062A008217e27B036a2e67F089E69a#code#F1#L1)

* BNB - [proposal payloads](https://bscscan.com/address/0x8c893864A7E7dE57C77cD907A44BBfFc5eC8dB36#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal adjusts the LTs and LTVs for similar assets listed on multiple Aave-V3 markets..

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xf1a776721bce33df14a498ab384bcaaafa85d1a766edb8028f0f791dcfa8378f](https://etherscan.io/tx/0xf1a776721bce33df14a498ab384bcaaafa85d1a766edb8028f0f791dcfa8378f)

```
- proposalId: 173
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x364d3500651a480d17b1727ae2585007be45b9a844219f88bb8ac8bbde1bfd39
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
      "payloadId": "180" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "83" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "55" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "50" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "52" 
    }, 
    { 
      "chain": "1088", 
      "accessLevel": "1", 
      "payloadsController": "0x2233F8A66A728FBa6E1dC95570B25360D07D5524", 
      "payloadId": "25" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "38" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "32" 
    }, 
    { 
      "chain": "534352", 
      "accessLevel": "1", 
      "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE", 
      "payloadId": "23" 
    }, 
    { 
      "chain": "56", 
      "accessLevel": "1", 
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627", 
      "payloadId": "22" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x364d3500651a480d17b1727ae2585007be45b9a844219f88bb8ac8bbde1bfd39" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/173.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/173.md)

**Payload reports**

* Ethereum - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/180.md)

* Polygon - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/83.md)

* Avalanche - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/55.md)

* Optimism - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/50.md)

* Arbitrum - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/52.md)

* Metis - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/25_forge.md)

* Base - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/38.md)

* Gnosis - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/32.md)

* Scroll - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/23_forge.md)

* BNB - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/22.md)

<br>

### Technical analysis

We have confirmed that the payload successfully modifies the LTV and LT of all assets on all V3-markets to the specified parameters on the IPFS. 

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

