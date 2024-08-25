# Proposal 155. Aave V3 Multichain Increase of WETH Optimal Ratio.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=155](https://vote.onaave.com/proposal/?proposalId=§55)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-increase-weth-optimal-ratio-to-90-on-all-aave-markets/18556](https://governance.aave.com/t/arfc-increase-weth-optimal-ratio-to-90-on-all-aave-markets/18556)

<br>

### Payloads

* Polygon - [proposal payloads](https://polygonscan.com/address/0xEbBF211C4817acaD620f33802A8409D47254E9b0#code#F1#L1) 

* Avalance - [proposal payloads](https://snowtrace.io/address/0x2ddbe1A78d0D0fc7E6b863BA0e771CC8C0Bc0122/contract/43114/code) 

* Metis - [proposal payloads](https://explorer.metis.io/address/0x128Ba0AdA7779C9D1bc3ddFCD5805fEA30C3A885/contract/1088/code) 

* Base - [proposal payloads](https://basescan.org/address/0x55F2c2028b631aA84e29074A6E7082cC64502122#code#F1#L1)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x4B4F11C8773748edD603BC30EF088b64D0BBaCc4#code#F1#L1)

* Scroll - [proposal payloads](https://scrollscan.com/address/0xd5516F8B3Ea54c15d6b41E14dEcf2456732D35e7#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal will increase WETH Optimal Usage Ratio to 90% from 80%.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x732f861d6309c543060af8796233dddb962ddc1dcfa2e63768f89e6ac91bf85b](https://etherscan.io/tx/0x732f861d6309c543060af8796233dddb962ddc1dcfa2e63768f89e6ac91bf85b)

```
- proposalId: 155
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xfe61618aec99c1250f1fe4e33b033c4893e7d44079f139f79f67fb676eedfb31
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
      "payloadId": "79" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "50" 
    }, 
    { 
      "chain": "1088", 
      "accessLevel": "1", 
      "payloadsController": "0x2233F8A66A728FBa6E1dC95570B25360D07D5524", 
      "payloadId": "24" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "32" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "28" 
    }, 
    { 
      "chain": "534352", 
      "accessLevel": "1", 
      "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE", 
      "payloadId": "20" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xfe61618aec99c1250f1fe4e33b033c4893e7d44079f139f79f67fb676eedfb31" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/155.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/155.md)

**Payload reports**

* Polygon - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/79.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/79.md)

* Avalanche - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/50.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/50.md)

* Metis - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/24_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/24_forge.md)

* Base - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/32.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/32.md)

* Gnosis - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/28.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/28.md)

* Scroll - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/20_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/20_forge.md)

<br>

### Technical analysis

We have verified that the payload setting up the optimal ratio correctly.
<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
