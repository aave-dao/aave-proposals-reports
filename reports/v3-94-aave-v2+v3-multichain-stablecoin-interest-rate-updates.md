# Proposal 94. Stablecoin Interest Rate Updates.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=94](https://vote.onaave.com/proposal/?proposalId=94)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-stablecoin-ir-curve-amendment-on-aave-v2-and-v3-04-22-2024/17450](https://governance.aave.com/t/arfc-stablecoin-ir-curve-amendment-on-aave-v2-and-v3-04-22-2024/17450)

<br>

### Payloads

* Ethereum V2- [proposal payloads](https://etherscan.io/address/0x26C0ab368D207c596d19E25b5bE3b7F1fAbF13aC#code#F1#L1)

* Ethereum V3- [proposal payloads](https://etherscan.io/address/0x41D6cf955ba45a3c3032b7C460D8B20b3a8023a9#code#F1#L1)

* Polygon V3- [proposal payloads](https://polygonscan.com/address/0x81674B9cdf884Aefae97579Ad16bdCf059916302#code#F1#L1)

* Avalanche V2- [proposal payloads](https://snowtrace.io/address/0x810B59706EE2852016913892a48EC26ff418BAA2/contract/43114/code)

* Avalanche V3- [proposal payloads](https://snowtrace.io/address/0x9062a4f0382f3DdEA6BC32e927ad8d11C1672adD/contract/43114/code)

* Optimism V3- [proposal payloads](https://optimistic.etherscan.io/address/0x504d3D47b7414f0329d653D8134fe22Fe2516c62#code#F1#L1)

* Arbitrum V3- [proposal payloads](https://arbiscan.io/address/0x7485a566092788B0F7428bdD8843A7eFc22F253a#code#F1#L1)

* Gnosis V3- [proposal payloads](https://gnosisscan.io/address/0x83381A5011cc65e6d153AFF1743B2cDfeC4b8cbf#code#F1#L1)

* Base V3- [proposal payloads](https://basescan.org/address/0xb6bE6e108cfd5c2ED03e9a98E8Aa010611a950AE#code#F1#L1)

* Scroll V3- [proposal payloads](https://scrollscan.com/address/0xAc9c64eA78e05901F477B8E1D2E4332EFc3E1211#code#F1#L1)

* BNB V3- [proposal payloads](https://bscscan.com/address/0xC113191a7fF22944740242140D6A79fC758fF3Cf#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal decreases stablecoin Interest Rate parameters across the v2+v3 platforms on multiple chains in order to align with the broader market.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x5fe651156ac1be77672e0fa9c9bbb6134b0e2cd080a8d517e07d0a1eab8ec767](https://etherscan.io/tx/0x5fe651156ac1be77672e0fa9c9bbb6134b0e2cd080a8d517e07d0a1eab8ec767)

```
- proposalId: 94
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xcded0cbbb1c8708cee734177abb444cdb8bdbaf9eb566188d7811de05f667a95
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
      "payloadId": "117" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "31" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "59" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "29" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "27" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "18" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "17" 
    }, 
    { 
      "chain": "534352", 
      "accessLevel": "1", 
      "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE", 
      "payloadId": "11" 
    }, 
    { 
      "chain": "56", 
      "accessLevel": "1", 
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627", 
      "payloadId": "13" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xcded0cbbb1c8708cee734177abb444cdb8bdbaf9eb566188d7811de05f667a95" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/94.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/94.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/117.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/117.md)

* Polygon - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/59.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/59.md)

* Avalanche - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/31.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/31.md)

* Optimism - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/29.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/29.md)

* Arbitrum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/27.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/27.md)

* Gnosis - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/17.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/17.md)

* Base - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/18.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/18.md)

* Scroll - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/11_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/11_forge.md)

* BNB - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/13.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/13.md)


<br>

### Technical analysis

We have verified that the payload decreases the variable slope1 of multiple stablecoins on the following chains:

- Ethereum V2:

    - USDC: 9%

    - USDT: 9%

    - DAI: 9%

- Ethereum V3:

    - USDC: 9%

    - USDT: 9%

    - DAI: 9%

    - FRAX: 9%

    - LUSD: 9%

    - pyUSD: 9%

    - crvUSD: 9%

- Avalanche V2:

    - USDC.e: 10%

    - USDT: 9%

    - DAI: 9%

- Avalanche V3:

    - USDC: 9%

    - USDT: 9%

    - DAI: 9%

    - FRAX: 9%

    - MAI: 9%

- Polygon V3:

    - USDC: 9%

    - USDT: 9%

    - DAI: 9%

    - MAI: 9%

    - EURA: 9%

    - EURS: 9%

    - jEUR: 9%

    - USDC.e: 10%

- Optimism V3:

    - USDC: 9%

    - USDT: 9%

    - DAI: 9%

    - sUSD: 9%

    - LUSD: 9%

    - MAI: 9%

    - USDC.e: 10%

- Arbitrum V3:

    - USDC: 9%

    - USDT: 9%

    - DAI: 9%

    - FRAX: 9%

    - LUSD: 9%

    - MAI: 9%

    - EURS: 9%

    - USDC.e: 10%

- Base V3:

    - USDbC: 10%

    - USDC: 9%

- BNB V3:

    - USDC: 9%

    - USDT: 9%

    - FDUSD: 9%

- Scroll V3:

    - USDC: 9%

- Gnosis V3:

    - USDC: 9%

    - WXDAI: 9%

    - EURe: 9%

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
