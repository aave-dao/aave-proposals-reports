# V3. Proposal 3. Aave v2/v3 Multichain - Rate strategies update

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=3](https://vote.onaave.com/proposal/?proposalId=3)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-stablecoin-ir-curves-updates/15838](https://governance.aave.com/t/arfc-chaos-labs-stablecoin-ir-curves-updates/15838)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal does changes on Slope 1 of multiple assets in multiple Aave v2 and v3 instances.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x1268c69d1eb569604864b112de9eff69ba2fbfa81f7156a6e55db444226f620a](https://etherscan.io/tx/0x1268c69d1eb569604864b112de9eff69ba2fbfa81f7156a6e55db444226f620a)


```
- proposalId: 3
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xa9b79871f27b840c5d04672f5b2ef16c753938cb80c6809087c1a47ad0fa2880
```

**createProposal() parameters**
```
{
  "payloads": [
    {
      "chain": "1",
      "accessLevel": 1,
      "payloadsController": "0xdabad81af85554e9ae636395611c58f7ec1aaec5",
      "payloadId": "44"
    },
    {
      "chain": "137",
      "accessLevel": 1,
      "payloadsController": "0x401b5d0294e23637c18fcc38b1bca814cda2637c",
      "payloadId": "25"
    },
    {
      "chain": "43114",
      "accessLevel": 1,
      "payloadsController": "0x1140cb7cafacc745771c2ea31e7b5c653c5d0b80",
      "payloadId": "12"
    },
    {
      "chain": "10",
      "accessLevel": 1,
      "payloadsController": "0x0e1a3af1f9cc76a62ed31ededca291e63632e7c4",
      "payloadId": "9"
    },
    {
      "chain": "42161",
      "accessLevel": 1,
      "payloadsController": "0x89644ca1bb8064760312ae4f03ea41b05da3637c",
      "payloadId": "8"
    },
    {
      "chain": "1088",
      "accessLevel": 1,
      "payloadsController": "0x2233f8a66a728fba6e1dc95570b25360d07d5524",
      "payloadId": "4"
    },
    {
      "chain": "8453",
      "accessLevel": 1,
      "payloadsController": "0x2dc219e716793fb4b21548c0f009ba3af753ab01",
      "payloadId": "6"
    },
    {
      "chain": "100",
      "accessLevel": 1,
      "payloadsController": "0x9a1f491b86d09fc1484b5fab10041b189b60756b",
      "payloadId": "3"
    }
  ],
  "votingPortal": "0x9b24c168d6a76b5459b1d47071a54962a4df36c3",
  "ipfsHash": "0xa9b79871f27b840c5d04672f5b2ef16c753938cb80c6809087c1a47ad0fa2880"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/3.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/3.md)

**Payloads report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/44.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/44.md)

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/25.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/25.md)

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/12.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/12.md)

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/9.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/9.md)

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/8.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/8.md)

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/6.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/6.md)

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/3.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/3.md)

*The proposal includes also a payload for Metis, but currently Aave seatbelt doesn't support Metis*

<br>

### Technical analysis

This proposal enacts the changes on the interest rate strategies' slope 1, on all assets affected **from 5% to 6%**. The payloads are the following:

[Aave v2 Ethereum](https://etherscan.io/address/0x91c24512Ec2965e4318B3Bcb3B16cB5b91C3337a#code#F1#L16)

Updating GUSD, sUSD, LUSD, DAI, FRAX, USDP, USDC, USDT.

<br>

[Aave v3 Ethereum](https://etherscan.io/address/0x8b97205b38F4aa3dA9Dc27Ff1CACbf16Af3636A9#code#F1#L16)

Updating LUSD, DAI, FRAX, USDC, USDT.

<br>

[Aave v2 Polygon](https://polygonscan.com/address/0x431504cff647d64254d8420A6d7b598d6B680Cc2#code#F1#L16)

Updating USDC, DAI, USDT.

<br>

[Aave v3 Polygon](https://polygonscan.com/address/0x9Fe29A547010772Aa4168c558E074CeFAdf81406#code#F1#L16)

Updating USDC, DAI, MAI, USDT.

<br>

[Aave v2 Avalanche](https://snowtrace.io/address/0x8652F56A632dfA31afb3A30933947B0A693D3834/contract/43114/code#F1#L16)

Updating USDC.e, USDT.e, DAI.e.

<br>

[Aave v3 Avalanche](https://snowtrace.io/address/0xdDf98cABd4B80492222C90401ae74757200118E6/contract/43114/code#F1#L16)

Updating MAI, USDt, USDC, FRAX, DAI.e.

<br>

[Aave v3 Optimism](https://optimistic.etherscan.io/address/0xfE30792b1b4d9216aa7c24E0B948a584ac3E1Fb9#code#F1#L16)

Updating USDC, sUSD, USDT, DAI, LUSD, MAI.

<br>

[Aave v3 Arbitrum](https://arbiscan.io/address/0x06f4915494Bd0d08c6c95D971B023463DC7A24dd#code#F1#L16)

Updating FRAX, MAI, LUSD, DAI, USDT, USDC.

<br>

[Aave v3 Metis](https://andromeda-explorer.metis.io/address/0xf7Afd747928485193B8B4c3146Ba63E8c3221239/contracts)

Updating m.USDC, m.USDT.

<br>

[Aave v3 Base](https://basescan.org/address/0xE7d9F770F27D1dBdE49bd04B947C3123D0A5b09B#code#F1#L16)

Updating USDC.

<br>

[Aave v3 Gnosis](https://gnosisscan.io/address/0x5e7590bbEFb804C3969C3A517fDd674858A70b01#code#F1#L16)

Updating USDC, wxDAI.

<br>

The proposal payload is consistent with the description in the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
