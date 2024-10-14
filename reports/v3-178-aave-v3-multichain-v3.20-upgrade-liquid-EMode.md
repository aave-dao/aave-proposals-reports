# Proposal 178. v3.20 Upgrade to Liquid EMode and StableDebt Removel.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=178](https://vote.onaave.com/proposal/?proposalId=178)

<br>

### Governance forum discussion

[https://governance.aave.com/t/bgd-aave-v3-2-liquid-emodes/19037](https://governance.aave.com/t/bgd-aave-v3-2-liquid-emodes/19037)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xb08c48659d6035698B0f1a61deA9C14a59f89622#code#F1#L28)

* EthereumLido - [proposal payloads](https://etherscan.io/address/0xf519083f06D2cD0Aa6dd780f0D06b2987a77F290#code#F1#L28)

* Ethereum EtherFi - [proposal payloads](https://etherscan.io/address/0x4E48C38a08388c29d9b71c657367e0D0cEf3A790#code#F1#L28)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x78DFB8b12bbCc65f415284f3C1ffA412678a725d#code#F1#L69)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x09262648Fce84992B68AbF216BfC47731F154462/contract/43114/code)

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0x09B5429d2c70b31379dAfAdC3F0fa015306a8d04#code#F1#L66)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0xAdDb96Fb6A795faf042DD25BD4710267C41D1F74#code#F1#L1)

* Metis - [proposal payloads](https://explorer.metis.io/address/0x84B08568906ee891de1c23175E5B92d7Df7DDCc4/contract/1088/code)

* Base - [proposal payloads](https://basescan.org/address/0x84B08568906ee891de1c23175E5B92d7Df7DDCc4#code#F1#L1)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0xe427FCbD54169136391cfEDf68E96abB13dA87A0#code#F1#L1)

* BNB - [proposal payloads](https://bscscan.com/address/0xe88fb4EAf67Ea87BB458e24C94BEf0EB02b5F449#code)

* Scroll - [proposal payloads](https://scrollscan.com/address/0x89654c66A6abd7174b525D05C2f4c442a615cee8#code)

* zkSync - [proposal payloads](https://era.zksync.network//address/0x9c0429dC6a8aA591B4d8bA0f3724987F5fB118E6#code#F1#L31)


<br>

## Certora analysis

<br>

### Proposal types

:scroll::small_red_triangle: contract upgrade

:moneybag: :receipt: asset transfer

<br>

### Context

The Aave 3.2 upgrade proposal aims to introduce significant improvements to the Aave protocol. The primary feature of this upgrade is the debut of Liquid eModes, which enhances the flexibility of Aave’s eModes by allowing assets to be listed in multiple categories and providing granular control over which assets can be used as collateral or borrowed. Additionally, the proposal finalizes the deprecation of stable borrowing by removing its residual artifacts, streamlining the protocol to reduce gas consumption and optimize code efficiency. The upgrade also includes provisions for reimbursing security audit costs, ensuring the protocol maintains its high standards of safety.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x07a8cecff5261f0f97e00dbe7b7eb635f9c83d30c3a7e7b27a8cda7c41654f52](https://etherscan.io/tx/0x07a8cecff5261f0f97e00dbe7b7eb635f9c83d30c3a7e7b27a8cda7c41654f52)

```
- proposalId: 178
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0x2e51e731f54ed0b5a0e3133b6f0de76c24ddf43e74c2c60ede057326ef7ae2d7
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
      "payloadId": "184" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "84" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "56" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "52" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "54" 
    }, 
    { 
      "chain": "1088", 
      "accessLevel": "1", 
      "payloadsController": "0x2233F8A66A728FBa6E1dC95570B25360D07D5524", 
      "payloadId": "26" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "39" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "33" 
    }, 
    { 
      "chain": "534352", 
      "accessLevel": "1", 
      "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE", 
      "payloadId": "24" 
    }, 
    { 
      "chain": "56", 
      "accessLevel": "1", 
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627", 
      "payloadId": "23" 
    }, 
    { 
      "chain": "324", 
      "accessLevel": "1", 
      "payloadsController": "0x2E79349c3F5e4751E87b966812C9E65E805996F1", 
      "payloadId": "6" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x2e51e731f54ed0b5a0e3133b6f0de76c24ddf43e74c2c60ede057326ef7ae2d7" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/178.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/178.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/184.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/184.md)

* EthereumLIdo - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/184.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/184.md)

* Ethereum EtherFi - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/184.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/184.md)

* Polygon - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/84.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/84.md)

* Avalanche - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/56.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/56.md)

* Optimism - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/52.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/52.md)

* Arbitrum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/54.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/54.md)

* Metis - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/26_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/26_forge.md)

* Base - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/39.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/39.md)

* Gnosis - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/33.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/33.md)

* BNB - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/23.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/23.md)

* Scroll - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/24_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/24_forge.md)

* zkSync - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/324/0x2E79349c3F5e4751E87b966812C9E65E805996F1/6_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/324/0x2E79349c3F5e4751E87b966812C9E65E805996F1/6_forge.md)

<br>

### Technical analysis

In the audit of the Aave 3.2 upgrade proposal, the primary focus was on verifying the correct implementation of Liquid eModes. The payload logic was thoroughly reviewed to ensure it allows for the increased flexibility of Liquid eModes, enabling assets to be listed in multiple eModes and offering more granular control over collateralization and borrowing. While the reset of eModeCategory bits in the reserve data storage was considered optional, this was not performed, and it is acceptable in the current context.

Secondary checks confirmed that the stableDebtToken address was correctly set to 0 on all assets, completing the final deprecation of stable borrowing. The audit also verified the transfer of 76,000 GHO to the BGD-controlled address for reimbursement of security procedure costs.

In addition to these checks, we confirmed the deployment included all necessary components, such as the new configuration engine, pool configurator, logic libraries, pool implementation, and both pool data provider and UI pool data provider. A thorough comparison of chain code diffs ensured consistency across implementations, and the seatbelt checks confirmed the bitmap configuration was correct.

Overall, these checks validate that the Aave 3.2 upgrade is correctly implemented and ready for deployment.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

