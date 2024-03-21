# Proposal 53. v3 Periphery maintenance.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=53](https://vote.onaave.com/proposal/?proposalId=53)

<br>

### Governance forum discussion

[https://governance.aave.com/t/bgd-technical-maintenance-proposals/15274/20](https://governance.aave.com/t/bgd-technical-maintenance-proposals/15274/20)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xAdDb96Fb6A795faf042DD25BD4710267C41D1F74#code#F1#L1)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x045950811Ed7B157158B4316F0e2F04726E3b4fa#code#F1#L1)

* Avalanche - [proposal payloads](https://snowscan.xyz/address/0x0e26e0bf83b4ec2cb0dcbc037bb01da5bb352eae#code#F1#L1)

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0xbe8554762a7A6D4343eA30954E2DbC5C638626a7#code#F1#L1)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0xB660d9F9745575B19a09fe0556c1b4C160966a32#code#F1#L1)

* Metis - [proposal payloads](https://explorer.metis.io/address/0xe427FCbD54169136391cfEDf68E96abB13dA87A0/contract/1088/code#F51#L36)

* Base - [proposal payloads](https://basescan.org/address/0x31A239f3e39c5D8BA6B201bA81ed584492Ae960F#code#F1#L1)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x15196D30Bc37d2fc5C718ffCd9d7687D76f3Ad1f#code#F1#L1)

* BNB - [proposal payloads](https://bscscan.com/address/0x8be473dCfA93132658821E67CbEB684ec8Ea2E74#code#F1#L1)

* Scroll(Price oracle sentinel) - [proposal payloads](https://scrollscan.com/address/0x1adfF3bbdcb54c9894Ad6a7A37Bc255D5764AEaA#code#F23#L1)

* Scroll(Stata tokens) - [proposal payloads](https://scrollscan.com/address/0x70Bf6EC6Fca41a7d08dCBB9909985AC0A4510B5E#code#F51#L1)

<br>

## Certora analysis

<br>

### Proposal types

:handshake: contract upgrade

<br>

### Context

This proposal is a batch of 2 proposals which are purely technical proposals to do minor improvements on two Aave v3’s periphery components:
- The first one is the activision of the Price oracle sentinel on the Scroll chain.

- The second one is fixing minor issues with the Static a token implementation.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x6a0919ba52636934b8042f77d987e05bc1e27cfa1f22667ea5cafd7a4d3ea9ad](https://etherscan.io/tx/0x6a0919ba52636934b8042f77d987e05bc1e27cfa1f22667ea5cafd7a4d3ea9ad)

```
- proposalId: 53
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0x2343307e9056837bfd3567bebd4774a67802e74bd097574cdb85e93a294407a2
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
      "payloadId": "83" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "42" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "16" 
    }, 
    { 
      "chain": "56", 
      "accessLevel": "1", 
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627", 
      "payloadId": "6" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "9" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "5" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "18" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "16" 
    }, 
    { 
      "chain": "1088", 
      "accessLevel": "1", 
      "payloadsController": "0x2233F8A66A728FBa6E1dC95570B25360D07D5524", 
      "payloadId": "7" 
    }, 
    { 
      "chain": "534352", 
      "accessLevel": "1", 
      "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE", 
      "payloadId": "3" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x2343307e9056837bfd3567bebd4774a67802e74bd097574cdb85e93a294407a2" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/53.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/53.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/83.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/83.md)

* Polygon V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/42.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/42.md)

* Avalanche V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/16.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/16.md)

* Optimism V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/18.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/18.md)

* Arbitrum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/16.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/16.md)

* Metis V3 - No seatbelt

* Base V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/9.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/9.md)

* Gnosis V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/5.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/5.md)

* BNB V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/6.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/6.md)

* Scroll V3 (Stata tokens) - No seatbelt

* Scroll V3 (Price oracle sentinel) - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/3_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/3_forge.md)

<br>

### Technical analysis

We have verified that the payload activates the Price oracle sentinel on the Scroll chain.

We have also verified that the payload upgrades the Static a token implementation of all stata tokens on the following chains: Ethereum, Polygon, Avalanche, Optimism, Arbitrum, Metis,
Base, Gnosis, BNB, Scroll and that the new implementation fixes the 2 following bugs:

- For reserves without a supplyCap the maxMint function on the static aToken would revert.

- The static-a-token is prone to permit griefing.


<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
