# Proposal 69. Stablecoin IR Updates.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=69](https://vote.onaave.com/proposal/?proposalId=69)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-stablecoin-ir-curve-amendment-on-aave-v2-and-v3/16864/5](https://governance.aave.com/t/arfc-stablecoin-ir-curve-amendment-on-aave-v2-and-v3/16864/5)

<br>

### Payloads

* Ethereum V2 - [proposal payloads](https://etherscan.io/address/0x5cBF152b414D1A29C4170D9B6eB507568974ca7d#code#F1#L1)

* Ethereum V3 - [proposal payloads](https://etherscan.io/address/0xd84aF55ec9A64AD3A3BBc0D3E009BF0D94682a91#code#F1#L1)

* Polygon V2 - [proposal payloads](https://polygonscan.com/address/0x4AA36B71eAD60695524cA4be160d56C530Eb2D7A#code#F1#L1)

* Polygon V3 - [proposal payloads](https://polygonscan.com/address/0x737E543B9dAb7Dd624aC05D6F2aFb310f035b7a4#code#F1#L1)

* Avalanche V2 - [proposal payloads](https://snowscan.xyz/address/0x0293f2b57e0f51490d87A5Fb59d95030E74dcf79#code#F1#L1)

* Avalanche V3 - [proposal payloads](https://snowscan.xyz/address/0x3A19355679Aa122016cd23de2fAeEb2c8f4C8d64#code#F1#L1)

* Optimism V3 - [proposal payloads](https://optimistic.etherscan.io/address/0x6047a14ec91cC2e0987Ac3306d761348D6543e37#code#F1#L1)

* Arbitrum V3 - [proposal payloads](https://arbiscan.io/address/0x371ce52c6A8f5a34Bc4faF4e50F16Cba74850a77#code#F1#L1)

* Base V3 - [proposal payloads](https://basescan.org/address/0x5FF75809E8Ce82a9a39Fea8a6d7BA03aB2298fb6#code#F1#L1)

* Gnosis V3 - [proposal payloads](https://gnosisscan.io/address/0x01978E782E701111ad97d70fceE19ce406154b62#code#F1#L1)

* Scroll V3 - [proposal payloads](https://scrollscan.com/address/0x4EbC22a1Fd177a62702BF29551DAadD373E0DD1c#code#F1#L1)

* BNB V3 - [proposal payloads](https://bscscan.com/address/0xb204Ade613044658DaC8997a54F4d686338cec2c#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal increases the interest rate of stablecoins across all Aave markets to align the rates with market values and maintain competitiveness.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x32c55df59c85555c3ac976899c489c976d0e1647f898053808eb1b2f9e14b93b](https://etherscan.io/tx/0x32c55df59c85555c3ac976899c489c976d0e1647f898053808eb1b2f9e14b93b)

```
- proposalId: 69
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xd089b245419090b798da1f8495c44d346b1d08c2d8888c10af9bca40762ea763
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
      "payloadId": "96" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "48" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "21" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "22" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "21" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "14" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "10" 
    }, 
    { 
      "chain": "534352", 
      "accessLevel": "1", 
      "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE", 
      "payloadId": "6" 
    }, 
    { 
      "chain": "56", 
      "accessLevel": "1", 
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627", 
      "payloadId": "9" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xd089b245419090b798da1f8495c44d346b1d08c2d8888c10af9bca40762ea763" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/69.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/69.md)

**Payload reports**

* Ethereum V2 & V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/96.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/96.md)

* Polygon V2 & V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/48.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/48.md)

* Avalanche V2 & V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/21.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/21.md)

* Optimism V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/22.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/22.md)

* Arbitrum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/21.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/21.md)

* Base V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/14.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/14.md)

* Gnosis V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/10.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/10.md)

* Scroll V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/6_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/6_forge.md)

* BNB V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/9.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/9.md)

<br>

### Technical analysis

We have verified that the payload modifies the rate strategy of the following stablecoins such that slope 1 is set to 12%:

* Ethereum:
    - V2: USDT, DAI, sUSD, USDC, GUSD, USDP, FRAX, LUSD
    - V3: USDC, DAI, USDT, LUSD, FRAX, crvUSD, PYUSD

* Polygon:
    - V2: USDT, DAI, USDC
    - V3: DAI, USDT, EURs, jEURs, EURA, USDC

* Avalanche:
    - V2: USDT.e, DAI.e
    - V3: DAI.e, USDT, USDC, FRAX, MAI

* Optimism:
    - V3: DAI, USDT, USDC, sUSD, LUSD, MAI

* Arbitrum:
    - V3: DAI, USDT, USDC, EURS, MAI, LUSD, FRAX

* Base:
    - V3: USDC

* Gnosis:
    - V3: USDC, WXDAI, EURe

* Scroll:
    - V3: USDC

* BNB:
    - V3: USDC, USDT FDUSD

and that the rate strategy of the following bridged USDC tokens is modified such that slope 1 is set to 13%:

* Polygon:
    - V3: USDC.e

* Avalanche:
    - V2: USDC.e

* Optimism:
    - V3: USDC.e

* Arbitrum:
    - V3: USDC.e

* Base:
    - V3: USDbC

In addition, we have verified that the optimal utilization ratio of USDC, USDT and DAI on the Ethereum V3 is raised to 92%.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
