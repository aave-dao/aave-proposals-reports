# Proposal 127. Increase Bridged USDC Reserve Factor Across All Deployments

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=127](https://vote.onaave.com/proposal/?proposalId=127)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-increase-bridged-usdc-reserve-factor-across-all-deployments/17787](https://governance.aave.com/t/arfc-increase-bridged-usdc-reserve-factor-across-all-deployments/17787)

[https://governance.aave.com/t/arfc-ethereum-v2-reserve-factor-adjustment/16764/13?u=luigy](https://governance.aave.com/t/arfc-ethereum-v2-reserve-factor-adjustment/16764/13?u=luigy)

[https://governance.aave.com/t/arfc-avalanche-v2-reserve-factor-adjustment/17040/8?u=luigy](https://governance.aave.com/t/arfc-avalanche-v2-reserve-factor-adjustment/17040/8?u=luigy)

[https://governance.aave.com/t/arfc-polygon-v2-borrow-rate-adjustments/17252/8?u=luigy](https://governance.aave.com/t/arfc-polygon-v2-borrow-rate-adjustments/17252/8?u=luigy)

[https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937/23?u=dd0sxx](https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937/23?u=dd0sxx)
<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x74b4E668999d39De1A0608467b4D42D4d2CA2a1c)
* Polygon  - [proposal payload1](https://polygonscan.com/address/0x31613CFdA7dFe373E832aCb4aE5C6863033d7A83)
* Polygon  - [proposal payload2](https://polygonscan.com/address/0x6d4406dFC416480519d8be1A2F6491430057Fb2f)
* Avalanche - [proposal payloads](https://snowtrace.io/address/0x6af4c429190ab3f778374be6b2fa27f800ff333f)
* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0xc30027598cD95fE8BB6E970e7511c28bE4F7A58c)
* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x252612e56DCe81c72A77a87AA197E37e3A1E18A3)
* Base - [proposal payloads](https://basescan.org/address/0x033f31c04dF0D4aAe22A7A7AA2E086B1b57e32a2)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal suggests reserve factor changes for some assets in AAVE V2 and V3 on Ethereum, Polygon, Avalanche, Optimism, Arbitrum and Base as well as variableRateSlope1 changes for some assets in AAVE V2 on Polygon.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xd0084b01a1577cbb15baa9f0aba0e67bae3689b1fadb3354f3f8ae162f413225](https://etherscan.io/tx/0xd0084b01a1577cbb15baa9f0aba0e67bae3689b1fadb3354f3f8ae162f413225)

```
- proposalId: 127
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xb7bd5818e6432b2b781eb9d948784ba13fe0e1ba0b8dcc395d75f76c687575e7
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
      "payloadId": "142" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "69" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "40" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "36" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "36" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "22" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xb7bd5818e6432b2b781eb9d948784ba13fe0e1ba0b8dcc395d75f76c687575e7" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/127.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/127.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/142.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/142.md)

* Polygon - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/69.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/69.md)

* Avalanche - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/40.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/40.md)

* Optimism - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/36.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/36.md)

* Arbitrum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/36.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/36.md)

* Base - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/22.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/22.md)

<br>

### Technical analysis

We have verified that the payload does the following:

- Changes the reserve factor of USDC.e on Polygon V3, Optimism V3 and Arbitrum V3 as well as USDbC on base V3 to 25%

- Changes the reserve factor of DAI, USDC, USDT and WETH on Ethereum V2 to 60% and the reserve factor of LINK and WBTC on Ethereum V2 to 65%

- Changes the reserve factor of DAIe, USDCe, USDTe, WAVAX and WETHe on Avalanche V2 to 55% and the reserve factor of WBTCe on Avalanche V2 to 60% 

- Changes the reserve factor of DAI, USDC and USDT on Polygon V2 to 99.99%

- Changes the variableRateSlope1 for DAI, USDT, wBTC, wETH, wUSDC, wMATIC on Polygon V2 to 11.25%, 11.25%, 6.25%, 6.25%, 11.25% and 8.25% respectively

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
