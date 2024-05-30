# Proposal 109. Migrate Robots to Chainlink Automation v2.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=109](https://vote.onaave.com/proposal/?proposalId=109)

<br>

### Governance forum discussion

[https://governance.aave.com/t/bgd-technical-maintenance-proposals/15274/36](https://governance.aave.com/t/bgd-technical-maintenance-proposals/15274/36)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x87C2a5b914BE15970657528d8662bd6F85a3E86c#code#F1#L1)

* Polygon Step 1 - [proposal payloads](https://polygonscan.com/address/0x9766194D65ad76C302b51443B8563dAe3D516E31#code#F1#L1)

* Polygon Step 2- [proposal payloads](https://polygonscan.com/address/0x0C5400172E5cbb01Fc030058fee5D212C5BC88D8#code#F1#L1)

* Avalanche Step 1 - [proposal payloads](https://snowscan.xyz/address/0xCe3C01D9c44C37CfB107868eBD911A99d1c83080#code#F1#L1)

* Avalanche Step 2 - [proposal payloads](https://snowscan.xyz/address/0x90cdbEAF9cC35A07acF90C1aAD7F6F1589e64Fd9#code#F1#L1)

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0x28956FEC07cfFc9586512BA0853356102FFF231c#code#F1#L1)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0xD288520b0eE0A005B40B96e63752064b3C0026dC#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:scroll::small_red_triangle: contract upgrade

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal migrates existing Aave robots from chainlink automation v1.2 to v2.1 and introduces gas-capped robots in order to limit execution based on network gas price.

The proposal also activate robots for refreshing liquidity mining rewards for static-a-tokens.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x8af911b85faf91ee6c550121bcf1d37abd5a38abe03d8839afff30d9d00b3e05](https://etherscan.io/tx/0x8af911b85faf91ee6c550121bcf1d37abd5a38abe03d8839afff30d9d00b3e05)

```
- proposalId: 109
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0x9d541c10fa619ee3f02e1e8712c710f47e60f126a1476d7df2c73b50afda4248
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "65" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "66" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "35" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "36" 
    }, 
    { 
      "chain": "1", 
      "accessLevel": "1", 
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5", 
      "payloadId": "130" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "32" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "29" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x9d541c10fa619ee3f02e1e8712c710f47e60f126a1476d7df2c73b50afda4248" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/109.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/109.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/130.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/130.md)

* Polygon Step 1 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/65.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/65.md)

* Polygon Step 2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/66.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/66.md) - seatbelt reverts due to the collector not having enough LINK, after the execution of Step 1 and than calling withdrawLink(), it will have.

* Avalanche Step 1 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/35.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/35.md)

* Avalanche Step 2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/36.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/36.md) - seatbelt reverts due to the collector not having enough LINK, after the execution of Step 1 and than calling withdrawLink(), it will have.

* Optimism - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/32.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/32.md)

* Arbitrum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/29.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/29.md)

<br>

### Technical analysis

We have verified that the payload Cancels the following Robots on the following chains:

- Ethereum:

    GSM SWAP FREEZE USDC ROBOT - 0xef6beca8d9543ec007bcea835af768b58f730c1f

    GSM SWAP FREEZE USDT ROBOT - 0x71381e6718b37c12155cb961ca3d374a8bffa0e5

    EXECUTION CHAIN ROBOT - 0x365d47ced3d7eb6a9bdb3814aa23cc06b2d33ef8

    GOVERNANCE CHAIN ROBOT - 0x011824f238aee05329213d5ae029e899e5412343

    VOTING CHAIN ROBOT - 0x2cf0fa5b36f0f89a5ea18f835d1375974a7720b8

- Polygon:

    EXECUTION CHAIN ROBOT - 0x249396a890f89d47f89326d7ee116b1d374fb3a9

    VOTING CHAIN ROBOT - 0xbe7998712402b6a63975515a532ce503437998b7

- Avalanche:

    EXECUTION CHAIN ROBOT - 0x7b74938583eb03e06042fcb651046baf0bf15644

    VOTING CHAIN ROBOT - 0x10e49034306eaa663646773c04b7b67e81ed0d52

- Optimism:

    EXECUTION CHAIN ROBOT - 0xa0195539e21a6553243344a3be6b874b5d3ec7b9

- Arbitrum:

    EXECUTION CHAIN ROBOT - 0x64093fe5f8cf62afb4377cf7ef4373537fe9155b

We have also checked the payloads register the following robots on the following chains:

- Ethereum:

    GSM SWAP FREEZE USDC ROBOT - 0xef6beCa8D9543eC007bceA835aF768B58F730C1f with 80 LINK

    GSM SWAP FREEZE USDT ROBOT - 0x71381e6718b37C12155CB961Ca3D374A8BfFa0e5 with 80 LINK

    EXECUTION CHAIN ROBOT - 0xBa37F9eDC52f57caFA3a13ddfD655797Cc4FE257 with 1500 LINK

    GOVERNANCE CHAIN ROBOT - 0x1996c281235D99bB3c6B8d2afbEb8ac6c7A39C11 with 2500 LINK

    VOTING CHAIN ROBOT - 0x7Ed0A6A294Cf085c90917c0ee1aa34e795932558 with 400 LINK

    STATIC A TOKEN ROBOT - 0xda82148a3944BBe442116f41cDb329b0edF11d41 with 200 LINK

- Polygon:

    EXECUTION CHAIN ROBOT - 0x249396a890F89D47F89326d7EE116b1d374Fb3A9 with 45 LINK

    VOTING CHAIN ROBOT - 0xbe7998712402B6A63975515A532Ce503437998b7 with 45 LINK

    STATIC A TOKEN ROBOT - 0x855FbD0D57fF5B1e8263e3cCDf3384545fbaF863 with 25 LINK

- Avalanche:

    EXECUTION CHAIN ROBOT - 0x7B74938583Eb03e06042fcB651046BaF0bf15644 with 45 LINK

    VOTING CHAIN ROBOT - 0x10E49034306EaA663646773C04b7B67E81eD0D52 with 45 LINK

    STATIC A TOKEN ROBOT - 0x8aD3f00e91F0a3Ad8b0dF897c19EC345EaB761c4 with 20 LINK

    PROOF OF RESERVE ROBOT - 0x7aE2930B50CFEbc99FE6DB16CE5B9C7D8d09332C with 15 LINK

- Optimism:

    EXECUTION CHAIN ROBOT - 0xa0195539e21A6553243344A3BE6b874B5d3EC7b9 with 45 LINK

    STATIC A TOKEN ROBOT - 0x861Be72d464b6F1C99880B9bE476D40e8F9b5Bce with 30 LINK

- Arbitrum:

    EXECUTION CHAIN ROBOT - 0x64093fe5f8Cf62aFb4377cf7EF4373537fe9155B with 45 LINK

    STATIC A TOKEN ROBOT - 0x0451f67bA61966C346daBAbB50a30Cc6A9A67C69 with 35 LINK

We have also checked the proposal refills the cross-chain-controller contract (part of aDI) on Ethereum with 1 ethereum from the collector.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
