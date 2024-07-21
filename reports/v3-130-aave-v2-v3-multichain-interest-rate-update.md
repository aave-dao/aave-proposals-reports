# Proposal 130. Stablecoin IR Curve Amendment.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=130](https://vote.onaave.com/proposal/?proposalId=130)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-stablecoin-ir-curve-amendment-on-aave-v2-and-v3-07-14-24/18252](https://governance.aave.com/t/arfc-stablecoin-ir-curve-amendment-on-aave-v2-and-v3-07-14-24/18252)

<br>

### Payloads

* Ethereum V2 - [proposal payloads](https://etherscan.io/address/0x8c8A63D53482C424f3c6c9Adc6b51053c3e0dCa8#code#F1#L1)

* Ethereum V3 - [proposal payloads](https://etherscan.io/address/0x9C5a3e2992FDc51dA7A93EB6060c1D5a370aa944#code#F1#L1)

* Polygon V3 - [proposal payloads](https://polygonscan.com/address/0xb4d095f86D8A1D6968520bf91322778A5844cf7f#code#F1#L1)

* Avalanche V3 - [proposal payloads](https://snowtrace.io/address/0x0a99A362d24cB7Ed4a4ab94494a7DFc71c408fD5/contract/43114/code)

* Optimism V3 - [proposal payloads](https://optimistic.etherscan.io/address/0x405Ad8dE7F75851132886E3e9893db9A6a96929c#code#F1#L1)

* Arbitrum V3 - [proposal payloads](https://arbiscan.io/address/0xE8740F06cC52f6e8dA8781AeAc88d3F043fd3757#code#F1#L1)

* Base V3 - [proposal payloads](https://basescan.org/address/0xfF179Aa658390b633847B6B6D109442439e456c5#code#F1#L1)

* Gnosis V3 - [proposal payloads](https://gnosisscan.io/address/0xD2Af3D004cDeE8c0Fe940895166060c9cCD72607#code#F1#L1)

* Scroll V3 - [proposal payloads](https://scrollscan.com/address/0xE37a1932c21895a6644eFd8150652af72A1b6cF7#code#F1#L1)

* BNB V3 - [proposal payloads](https://bscscan.com/address/0xf27992Bb64E9043b8622B5bAbA7943cE82d734e7#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal suggests to lower the interest rates of all stablecoins across all networks due to changes in DSR rates which are expected to impact stablecoin rates across DeFi.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x7d25e9894dfc27f6443c8051aad2251368a787d436c3be74ef150ec70eb426d4](https://etherscan.io/tx/0x7d25e9894dfc27f6443c8051aad2251368a787d436c3be74ef150ec70eb426d4)

```
- proposalId: 130
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x2e8cee15c55cf4031ba0bc234478cfb0a9ced14e6b7d3967c32a9fbe0626178e
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
      "payloadId": "144" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "70" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "41" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "37" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "37" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "24" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "22" 
    }, 
    { 
      "chain": "534352", 
      "accessLevel": "1", 
      "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE", 
      "payloadId": "14" 
    }, 
    { 
      "chain": "56", 
      "accessLevel": "1", 
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627", 
      "payloadId": "16" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x2e8cee15c55cf4031ba0bc234478cfb0a9ced14e6b7d3967c32a9fbe0626178e" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/130.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/130.md)

**Payload reports**

* Ethereum V2+V3 - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/144.md)

* Polygon V3 - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/70.md)

* Avalanche V3 - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/41.md)

* Optimism V3 - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/37.md)

* Arbitrum V3 - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/37.md)

* Base V3 - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/24.md)

* Gnosis V3 - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/22.md)

* Scroll V3 - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/14_forge.md)

* BNB V3 - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/16.md)
<br>

### Technical analysis

We have verified that the payload reduces slope 1 of all the stablecoins that are specified in the IPFS to 6.5%, 0.5% less than the expected DSR.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

