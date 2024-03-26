# Proposal 56. Update a.DI implementation and CCIP adapters.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=56](https://vote.onaave.com/proposal/?proposalId=56)

<br>

### Governance forum discussion

[https://governance.aave.com/t/bgd-technical-maintenance-proposals/15274/21](https://governance.aave.com/t/bgd-technical-maintenance-proposals/15274/21)

<br>

### Payloads

* Ethereum - [proposal payload](https://etherscan.io/address/0x6093e2f483D33d5B4fEaFe179557cE3802409487#code#F1#L1)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x11A24Eb29e152C0Bf51999612389421CaB56105E#code#F1#L16)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xD6b05D12FB79a09DfB63A005a12D65f196Ec173F/contract/43114/code#F1#L45)

* BNB - [proposal payloads](https://bscscan.com/address/0x8B9D9e67198221FdFE3DDFC175BE41fBF8C143e7#code#F1#L1)

* Base - [proposal payloads](https://basescan.org/address/0xc03421E9a303a7635BfB995b142dF15a9A440Cbc#code#F1#L1)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0xF8d99c4F089fB4210141285E7FeF4c7ad2C7D576#code#F1#L1)

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0xB00bAaa57893886CA06dF36554E31439F8239C2d#code#F1#L1)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0xCd320CA435193b4A9B04d0a02C777b5E8902C9b4#code#F1#L1)

* Metis - [proposal payloads](https://explorer.metis.io/address/0x03729F178f27bfE72AD53E425B474b61B8291b22/contract/1088/code)

* Scroll - [proposal payloads](https://scrollscan.com/address/0x2F6CF226843042a6B84Dcf785e3192847782C35E#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:scroll::small_red_triangle: contract upgrade
:handshake: permission granting or revoking

<br>

### Context

This proposal upgrades the cross-chain controller to introduce some off-chain visibility changes to the code. In addition it updates CCIP Bridge Adapters.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x194851b5eb092b48d31aae00507f0b856d4aaa2f731967119a584cdd75f60ef1](https://etherscan.io/tx/0x194851b5eb092b48d31aae00507f0b856d4aaa2f731967119a584cdd75f60ef1)

```
- proposalId: 56
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0xfd641d22acacbcc09b476a08bb21c127dfc6d53b511bc7dc022135387159e3fd
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
      "payloadId": "85" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "45" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "18" 
    }, 
    { 
      "chain": "56", 
      "accessLevel": "1", 
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627", 
      "payloadId": "7" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "10" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "7" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "20" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "18" 
    }, 
    { 
      "chain": "1088", 
      "accessLevel": "1", 
      "payloadsController": "0x2233F8A66A728FBa6E1dC95570B25360D07D5524", 
      "payloadId": "8" 
    }, 
    { 
      "chain": "534352", 
      "accessLevel": "1", 
      "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE", 
      "payloadId": "4" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xfd641d22acacbcc09b476a08bb21c127dfc6d53b511bc7dc022135387159e3fd" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/56.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/56.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/85.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/85.md)

* Polygon V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/45.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/45.md)

* Avalanche V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/18.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/18.md)

* BNB V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/7.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/7.md)

* Base V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/10.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/10.md)

* Gnosis V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/7.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/7.md)

* Optimism V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/20.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/20.md)

* Arbitrum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/18.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/18.md)

* Metis V3 - No Report

* Scroll - No Report

<br>

### Technical analysis

We verified that the payloads upgrade the cross-chain controller implementation on all the mentioned networks to the specified addresses. In addition, we verified that CCIP adapters were updated to new implementations, disabling the old ones instead.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
