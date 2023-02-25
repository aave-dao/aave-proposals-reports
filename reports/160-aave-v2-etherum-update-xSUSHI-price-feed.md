# Proposal 160. Aave v2 Ethereum - update xSUSHI price feed

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=160](https://app.aave.com/governance/proposal/?proposalId=160)

<br>

### Governance forum discussion

[https://governance.aave.com/t/bgd-swap-of-price-feed-of-xsushi-on-aave-v2-ethereum/11901](https://governance.aave.com/t/bgd-swap-of-price-feed-of-xsushi-on-aave-v2-ethereum/11901)

<br>

## BGD analysis

<br>

### Proposal types

:crystal_ball: oracle-addition

<br>

### Context

This proposal updates the oracle price feed for xSUSHI on Aave v2 Ethereum, from a custom adapter contract to the Chainlink calculated xSUSHI/ETH.
The rationale behind is to be consistent with the idea of using off-chain calculated feeds for assets like xSUSHI, whose prices are primarily correlated with an underlying (SUSHI).


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x84fa9feb8dfb61eb96f53d1ab6a1861366cbb3e6a0bd11875d442d6262001755](https://etherscan.io/tx/0x84fa9feb8dfb61eb96f53d1ab6a1861366cbb3e6a0bd11875d442d6262001755)

```
- id: 160
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x3105c276558dd4cf7e7be71d73be8d33bd18f211]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16677100
- endBlock: 16696300
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x62eecfcd8fa8264bf4c95014fbf3e4cc7bce8d91d1e58cede18de038660ea8be
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/160.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/160.md)

<br>

### Technical analysis

The [proposal payload](https://etherscan.io/address/0x3105C276558Dd4cf7E7be71d73Be8D33bD18F211#code#F3#L1) simply interacts with the [AaveOracle](https://etherscan.io/address/0xA50ba011c48153De246E5192C8f9258A2ba79Ca9#code) of Aave v2 Ethereum to replace the current price feed for xSUSHI with the [Chainlink calculated xSUSHI/ETH](https://etherscan.io/address/0xF05D9B6C08757EAcb1fbec18e36A1B7566a13DEB#code), by calling the `setAssetSources()` function.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD wrote the payload.

:x: With BGD writing the payload, at least another party reviewed it.
