# Proposal 121. Optimize ETH-correlated asset parameters.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=121](https://vote.onaave.com/proposal/?proposalId=121)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-optimize-eth-correlated-asset-parameters/17886](https://governance.aave.com/t/arfc-optimize-eth-correlated-asset-parameters/17886)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x1f49d2d8Fe885c9339B32088ca9058774673aDD8#code#F1#L1)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x4c7BbD2b7E30a470627d8D7eF092B38e48919630#code#F1#L1)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x6fCa0329dCeB3bB20091a9084736e6573F3Bb4A7/contract/43114/code)

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0xacF6d876779F5974Bc1d525a35F8cEb3FB247177#code#F1#L1)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x73b55d60982417d86562608B816E199bd7b3fD9C#code#F1#L1)

* Metis - [proposal payloads](https://explorer.metis.io/address/0x592921fe80C04943ca7d4a8Af9849b566714adA0/contract/1088/code)

* Base - [proposal payloads](https://basescan.org/address/0xCABd01E2c57942aAD6dE862816647747753d7116#code#F1#L1)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x99919A6770081c7388D9b055874f4E08367D2ff8#code#F1#L1)

* Scroll - [proposal payloads](https://scrollscan.com/address/0x017E77d5184C0432421c9bAbCC1F6FED50d07203#code#F1#L1)

* BNB - [proposal payloads](https://bscscan.com/address/0xf9Ec102cC88B949DFe41e1eC8d9f8117047dB5EC#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal updates parameters on ETH-correlated assets and coordinate caps management to improve Aave efficiency.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x581f133ca4c7dd9085d5318beb570363b9bf083fbca355099a5fcaf4f2d803d2](https://etherscan.io/tx/0x581f133ca4c7dd9085d5318beb570363b9bf083fbca355099a5fcaf4f2d803d2)

```
- proposalId: 121
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xfdc35cc906ad3f5d5f2a051167e87d95abd104a7f30bf5910b5adb23f84e4df2
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
      "payloadId": "138" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "68" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "38" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "35" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "33" 
    }, 
    { 
      "chain": "1088", 
      "accessLevel": "1", 
      "payloadsController": "0x2233F8A66A728FBa6E1dC95570B25360D07D5524", 
      "payloadId": "18" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "21" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "21" 
    }, 
    { 
      "chain": "534352", 
      "accessLevel": "1", 
      "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE", 
      "payloadId": "13" 
    }, 
    { 
      "chain": "56", 
      "accessLevel": "1", 
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627", 
      "payloadId": "15" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xfdc35cc906ad3f5d5f2a051167e87d95abd104a7f30bf5910b5adb23f84e4df2" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/121.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/121.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/138.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/138.md)

* Polygon V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/68.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/68.md)

* Avalanche V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/38.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/38.md)

* Optimism V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/35.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/35.md)

* Arbitrum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/33.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/33.md)

* Metis V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/18_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/18_forge.md)

* Base V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/21.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/21.md)

* Gnosis V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/21.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/21.md)

* Scroll V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/13_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/13_forge.md)

* BNB V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/15.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/15.md)

<br>

### Technical analysis

We have verified that the payloads modify the variable slope 1 of the wETH to 2.7% on all v3 markets.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
