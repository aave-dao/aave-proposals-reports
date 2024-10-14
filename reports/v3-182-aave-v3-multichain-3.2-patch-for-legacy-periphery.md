# Proposal 182. 3.2 patch for legacy periphery.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=182](https://vote.onaave.com/proposal/?proposalId=182)

<br>

### Governance forum discussion

[https://governance.aave.com/t/bgd-technical-maintenance-proposals/15274/45](https://governance.aave.com/t/bgd-technical-maintenance-proposals/15274/45)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x55c09b4Df32606667dBdF7dc846417bFb4Cec776#code#F1#L1)

* EthereumLido - [proposal payloads](https://etherscan.io/address/0xF4AbB0d80C1E5D4Be3dCd38a864AD5D8bFDe0ac3#code#F1#L1)

* Ethereum EtherFi - [proposal payloads](https://etherscan.io/address/0x56496FA0C8AB691dAe9632320963862108775ab2#code#F1#L1)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x2Efe215aE82339fa059bb9d611E4cC858cfe9Df6#code#F1#L1)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xA434D495249abE33E031Fe71a969B81f3c07950D/contract/43114/code)

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0xAdDb96Fb6A795faf042DD25BD4710267C41D1F74#code#F1#L1)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0xF5eA8A01d4e0456B605dC0f1EC4E401a8cA6397A#code#F1#L1)

* Metis - [proposal payloads](https://explorer.metis.io/address/0x61637B1EF7e9A102e50B661D3d7dbe19ef93347e/contract/1088/code)

* Base - [proposal payloads](https://basescan.org/address/0x29081f7aB5a644716EfcDC10D5c926c5fEe9F72B#code#F1#L1)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0xD410270dadBA6CAB0b3523136b79ab3a19CCecc8#code#F1#L1)

* BNB - [proposal payloads](https://bscscan.com/address/0x3cd1dFB81C50A5300C60a181ED145a7286d81e0a#code#F1#L1)

* Scroll - [proposal payloads](https://scrollscan.com/address/0x82dcCF206Ae2Ab46E2099e663F70DeE77caE7778#code#F1#L1)

* zkSync - [proposal payloads](https://era.zksync.network//address/0x449e788367f32a6E19C54557A4D36FA8bc4C2eB4#code#F1#L1)


<br>

## Certora analysis

<br>

### Proposal types

:scroll::small_red_triangle: contract upgrade

<br>

### Context

This proposal is a ptach for the 3.2 upgrade which was executed in [AIP 178](https://vote.onaave.com/proposal/?proposalId=178).
The patch upgrades the pool contract across all markets, to add an extra fallback on the getReserveData() view function, allowing for integrators unable to update peripheral contracts (Aave Pool Data Provider) to still be compatible with v3.2.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xa5a6ae4742951654b8350973f2d7bcfef19a77b8e2f2cd62fab5c30f5e4b312a](https://etherscan.io/tx/0xa5a6ae4742951654b8350973f2d7bcfef19a77b8e2f2cd62fab5c30f5e4b312a)

```
- proposalId: 182
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0xeaee8d7ba5887bceebc3d403a4f28035e4fb33312effe067d5e291d0cb1a2963
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
      "payloadId": "189" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "85" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "57" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "53" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "55" 
    }, 
    { 
      "chain": "1088", 
      "accessLevel": "1", 
      "payloadsController": "0x2233F8A66A728FBa6E1dC95570B25360D07D5524", 
      "payloadId": "27" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "40" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "34" 
    }, 
    { 
      "chain": "534352", 
      "accessLevel": "1", 
      "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE", 
      "payloadId": "25" 
    }, 
    { 
      "chain": "56", 
      "accessLevel": "1", 
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627", 
      "payloadId": "24" 
    }, 
    { 
      "chain": "324", 
      "accessLevel": "1", 
      "payloadsController": "0x2E79349c3F5e4751E87b966812C9E65E805996F1", 
      "payloadId": "7" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xeaee8d7ba5887bceebc3d403a4f28035e4fb33312effe067d5e291d0cb1a2963" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/182.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/182.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/189.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/189.md)

* Polygon - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/85.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/85.md)

* Avalanche - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/57.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/57.md)

* Optimism - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/53.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/53.md)

* Arbitrum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/55.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/55.md)

* Metis - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/27_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/27_forge.md)

* Base - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/40.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/40.md)

* Gnosis - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/34.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/34.md)

* Scroll - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/25_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/25_forge.md)

* BNB - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/24.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/24.md)

* zkSync - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/324/0x2E79349c3F5e4751E87b966812C9E65E805996F1/7_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/324/0x2E79349c3F5e4751E87b966812C9E65E805996F1/7_forge.md)

<br>

### Technical analysis

We have verified that the proposal upgrades all the pools on all the v3 markets to match the latest patch which includes an extra fallback on the getReserveData() view function which will be a dummy stable debt token (one that existed before the 3.2 patch), which will always return 0 on total supply and other filed such as balanceOf, in order to return real data and prevent reverts of the function.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

