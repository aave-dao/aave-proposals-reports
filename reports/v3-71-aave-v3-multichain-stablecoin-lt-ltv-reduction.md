# Proposal 71. Generalized LT/LTV Reduction on Aave.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=71](https://vote.onaave.com/proposal/?proposalId=71)

<br>

### Governance forum discussion

[https://governance.aave.com/t/generalized-lt-ltv-reduction-on-aave/16766](https://governance.aave.com/t/generalized-lt-ltv-reduction-on-aave/16766)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xd56232B949Dd7E70E95Bb99514Eaf9Dba160d042)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x22b2d204cbBD33dbddf37a63795E3c7F280b56b2)

* Avalanche - [proposal payloads](https://snowscan.xyz/address/0x54Bdd028Cf5CDB252990093AccEdAf7995E54EF6)

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0x11b8cEB0D53c3810959be617B5C22FA63E2181aC)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x057A200E6ceD7a4447f7da70e9815D62019C5544)

* Base - [proposal payloads](https://basescan.org/address/0x5D9584E01Cbde091E66F9444F243e4befAad38B4)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x1B8f08D90076c1E0D9e92cb66eD99f9E77dCe2cb)

* BNB - [proposal payloads](https://bscscan.com/address/0xE2593fA0709C80fE48ac163d0f859DEAE5CF0747)

* Scroll - [proposal payloads](https://scrollscan.com/address/0x1C3D81Af0bF0a6558B891F51BA708A9de9A92cC1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal reduces the LTV and LT of stablecoins across markets as a reaction to reduce potential risk of long-tailed assets used as debt, given the current low collateralization usage of stablecoins.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xd3c63e695d68a8eba19fde61a6043d987e316e3d768faf96759161f897f2111f](https://etherscan.io/tx/0xd3c63e695d68a8eba19fde61a6043d987e316e3d768faf96759161f897f2111f)

```
- proposalId: 71
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x293815b30e809a40f094c7a6164a60bc5d306cc915455bbbfb1c083fd1161f1d
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
      "payloadId": "98" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "51" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "22" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "24" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "23" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "16" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "12" 
    }, 
    { 
      "chain": "56", 
      "accessLevel": "1", 
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627", 
      "payloadId": "10" 
    }, 
    { 
      "chain": "534352", 
      "accessLevel": "1", 
      "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE", 
      "payloadId": "8" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x293815b30e809a40f094c7a6164a60bc5d306cc915455bbbfb1c083fd1161f1d" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/71.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/71.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/98.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/98.md)

* Polygon V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/51.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/51.md)

* Avalanche V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/22.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/22.md)

* Optimism V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/24.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/24.md)

* Arbitrum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/23.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/23.md)

* Base V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/16.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/16.md)

* Gnosis V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/12.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/12.md)

* BNB V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/10.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/10.md)

* Scroll V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/8_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/8_forge.md)

<br>

### Technical analysis

We have verified that the payload modifies the LTV and LT of the following stablecoins to the following values respectively:

* Ethereum V3:
    - USDT - 76%, 79%
    - DAI - 76%, 79%
    - USDC - 76%, 79%
    - sDAI - 76%, 79%

* Polygon V3:
    - USDT - 76%, 79%
    - DAI - 76%, 79%
    - USDC - 76%, 79%
    - USDC.e - 76%, 79%

* Avalanche V3:
    - USDT - 75%, 78%
    - DAI - 75%, 80%
    - USDC - 80%, 85%

* Optimism V3:
    - USDT - 76%, 79%
    - DAI - 75%, 80%
    - USDC - 76%, 79%
    - USDC.e - 78%, 84%

* Arbitrum V3:
    - USDT - 76%, 79%
    - DAI - 76%, 79%
    - USDC - 76%, 79%
    - USDC.e - 76%, 79%

* Base V3:
    - USDC - 76%, 79%
    - USDbC - 76%, 79%

* Gnosis V3:
    - xDAI - 76%, 79%
    - USDC - 76%, 79%
    - sDAI - 76%, 79%

* BNB V3:
    - USDT - 76%, 79%
    - USDC - 76%, 79%

* Scroll V3:
    - USDC - 76%, 79%

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
