# Proposal 55. Stablecoin Harmonization.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=55](https://vote.onaave.com/proposal/?proposalId=55)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-stablecoin-harmonization-and-asset-parameters-optimization/16802](https://governance.aave.com/t/arfc-stablecoin-harmonization-and-asset-parameters-optimization/16802)

<br>

### Payloads

* Ethereum - [proposal payload](https://etherscan.io/address/0xF5a40B84E4c73d9A6dE5C0950D7430F6D43b3D2C#code#F1#L1)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x841b690FACc0C1DcD36d054F7CAfbC006F48eD66#code#F1#L1)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x27EfDEf036B668fbfe676429C6176E31335Ecc8B/contract/43114/code#F1#L74)

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0x231349e69718c00a7D95F953F45C25402d35edae#code#F1#L1)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x868b4BC72f3aD129b3c5805b19ce2a18849BC1Ae#code#F1#L1)

* Metis - [proposal payloads](https://explorer.metis.io/address/0x7c97C9EA58627491AEE1F9A3240d4Df47EDae739/contract/1088/code)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0xFfcaB3B06ca6D53B8487f40cF4e14032B769044E#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal aims to slowly off-board as collateral on Aave V3 certain tokens and stablecoins that didn't gain expected traction due to risk considerations. This is part of a strategy to focus collateral in the market on USDC and USDT. The off-boarding is done by slow increase of the reserve factor for these assets, slow lowering of the liquidation thresholds, and freezing some assets.
The idea is to also create a correlation where possible between market configurations across different chains.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x3ad148e874cb9ca26b9e60d028c3a76798f02754158337dee9f7ad853a072ca8](https://etherscan.io/tx/0x3ad148e874cb9ca26b9e60d028c3a76798f02754158337dee9f7ad853a072ca8)

```
- proposalId: 55
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x58817985af9b5d3209b397088902ea3471b5afc3ebf5846b6dac029e75ac9fa0
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
      "payloadId": "84" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "44" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "17" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "19" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "17" 
    }, 
    { 
      "chain": "1088", 
      "accessLevel": "1", 
      "payloadsController": "0x2233F8A66A728FBa6E1dC95570B25360D07D5524", 
      "payloadId": "9" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "6" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x58817985af9b5d3209b397088902ea3471b5afc3ebf5846b6dac029e75ac9fa0" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/55.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/55.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/84.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/84.md)

* Polygon V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/44.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/44.md)

* Avalanche V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/17.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/17.md)

* Optimism V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/19.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/19.md)

* Arbitrum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/17.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/17.md)

* Metis V3 - No Report

* Gnosis V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/6.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/6.md)

<br>

### Technical analysis

We verified that the payloads effectively freeze the following assets on the following chains:

* Ethereum V3:
    - STG
    - KNC
    - FXS

* Polygon V3:
    - agEUR

* Arbitrum V3:
    - EURS

We verified that the payloads effectively modifying zeroing the LTV of the following assets on the following chains:

* Ethereum V3:
    - LUSD
    - FRAX
    - STG
    - KNC
    - FXS

* Avalanche V3:
    - WBTCe
    - FRAX

* Arbitrum V3:
    - EURS
    - FRAX

We verified that the payloads effectively decrease the liquidation threshold the following assets by 3% on the following chains:

* Ethereum V3:
    - LUSD: 80% -> 77%
    - BAL: 62% -> 59%
    - UNI: 77% -> 74%
    - FRAX: 75% -> 72%
    - STG: 40% -> 37%
    - KNC: 40% -> 37%
    - FXS: 45% -> 42%

* Polygon V3:
    - BAL: 45% -> 42%

* Avalanche V3:
    - WBTCe: 70% -> 67%
    - FRAX: 80% -> 77%

* Arbitrum V3:
    - EURS: 70% -> 67%
    - FRAX: 75% -> 72%

Finally we verified that the payloads effectively increases the reserve factor the following assets according to the mentioned specification on the following chains:

* Ethereum V3:
    - DAI: 10% -> 25%
    - LUSD: 10% -> 20%
    - FRAX: 10% -> 20%

* Polygon V3:
    - DAI: 10% -> 25%
    - EURS: 10% -> 20%

* Avalanche V3:
    - DAIe: 10% -> 25%
    - FRAX: 10% -> 20%

* Optimism V3:
    - DAI: 10% -> 25%
    - LUSD: 10% -> 20%
    - sUSD: 10% -> 20%

* Arbitrum V3:
    - DAI: 10% -> 25%
    - EURS: 10% -> 20%
    - LUSD: 10% -> 20%
    - FRAX: 10% -> 20%

* Metis V3:
    - mDAI: 10% -> 25%

* Gnosis V3:
    - WXDAI: 10% -> 25%
    - EURe: 15% -> 20%

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
