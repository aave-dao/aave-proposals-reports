# Proposal 184. Update of Emergency Guardians

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=184](https://vote.onaave.com/proposal/?proposalId=184)

<br>

### Governance forum discussion

[https://governance.aave.com/t/bgd-technical-maintenance-proposals/15274/48](https://governance.aave.com/t/bgd-technical-maintenance-proposals/15274/48)

<br>

### Payloads

* Ethereu V3 - [proposal payloads](https://etherscan.io/address/0xb3EEAeeBE92b76eDC776f013913629E7fc7FA607#code#F1#L25)

* Ethereum V2 - [proposal payloads](https://etherscan.io/address/0x24FD0CD7f15E252eF57929f6449Fbb8838910860#code)

* Ethereum AMM - [proposal payloads](https://etherscan.io/address/0x46bbeC9ccFb44a457B6FBea6054Feb8D921aE108#code)

* Polygon V2 - [proposal payloads](https://polygonscan.com/address/0x46f285361364d415721e9e3C1AF76B1CE237cbAe#code#F1#L1)

* Polygon V3 - [proposal payloads](https://polygonscan.com/address/0x1b7802EA883dADdcfF753ACb0996DE33ff26D0Bd#code#F1#L6)

* Avalanche V2 - [proposal payloads](https://snowtrace.io/address/0xd62B1258bDbf8d6809c269327b37DCee3c4f6459/contract/43114/code)

* Avalanche V3 - [proposal payloads](https://snowtrace.io/address/0x56F5371F548344E7ba1A47C57efB4A3FDdA425B2/contract/43114/code)

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0x2986D0391e1E80899D00948231D5d2128A39F797#code#F1#L1)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x10424E15788fEC8C674d7c773C95E2fFe0EA7835#code#F1#L1)

* Metis - [proposal payloads](https://explorer.metis.io/address/0x50A226C3DF3172D1f2E3545c44E3637Db633f8F4/contract/1088/code)

* Base - [proposal payloads](https://basescan.org/address/0x4A3C0B2515164f6042eEE83A0BACa9CD8e3CDA9f#code#F1#L1)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x9EE6113282790c3541494b64F38F921E7E0D5C87#code#F1#L1)

* BNB - [proposal payloads](https://bscscan.com/address/0x688d52403877E99a72671037f32f74C2945C0F4C#code#F1#L1)

* Scroll - [proposal payloads](https://scrollscan.com/address/0xA465Bf9a77C3f1597bdfF830a97DE1940102D3B0#code#F1#L1)


<br>

## Certora analysis

<br>

### Proposal types

:handshake: permission granting or revoking

<br>

### Context

This proposal aims to update emergency roles (protocol & governance) to the new elected Aave Protocol & Emergency Guardians.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x0bbcaa05b2b27fec028b049e48894c0e58111bbc0d75d8911772e4d4a19fb3df](https://etherscan.io/tx/0x0bbcaa05b2b27fec028b049e48894c0e58111bbc0d75d8911772e4d4a19fb3df)

```
- proposalId: 184
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0xb39e261d5441ad39505291b12cb76a6a03790ff18395b62738e01e3ef0fb3c66
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
      "payloadId": "191" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "86" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "58" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "54" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "56" 
    }, 
    { 
      "chain": "1088", 
      "accessLevel": "1", 
      "payloadsController": "0x2233F8A66A728FBa6E1dC95570B25360D07D5524", 
      "payloadId": "28" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "42" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "35" 
    }, 
    { 
      "chain": "534352", 
      "accessLevel": "1", 
      "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE", 
      "payloadId": "26" 
    }, 
    { 
      "chain": "56", 
      "accessLevel": "1", 
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627", 
      "payloadId": "25" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xb39e261d5441ad39505291b12cb76a6a03790ff18395b62738e01e3ef0fb3c66" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/184.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/184.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/191.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/191.md)

* Polygon - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/86.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/86.md)

* Avalanche - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/58.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/58.md)

* Optimism - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/54.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/54.md)

* Arbitrum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/56.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/56.md)

* Base - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/42.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/42.md)

* Gnosis - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/35.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/35.md)

* BNB - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/25.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/25.md)


<br>

### Technical analysis

We have verified that the proposal updates the Protocol and the Governance Guardiand roles to the specified addresses in the AIP & forum properly.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

