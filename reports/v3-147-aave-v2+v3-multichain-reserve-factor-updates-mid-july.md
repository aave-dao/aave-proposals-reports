# Proposal 147. Reserve Factor Updates Mid July.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=147](https://vote.onaave.com/proposal/?proposalId=147)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-increase-bridged-usdc-reserve-factor-across-all-deployments/17787/5](https://governance.aave.com/t/arfc-increase-bridged-usdc-reserve-factor-across-all-deployments/17787/5)

[https://governance.aave.com/t/arfc-ethereum-v2-reserve-factor-adjustment/16764/14](https://governance.aave.com/t/arfc-ethereum-v2-reserve-factor-adjustment/16764/14)

[https://governance.aave.com/t/arfc-avalanche-v2-reserve-factor-adjustment/17040/9](https://governance.aave.com/t/arfc-avalanche-v2-reserve-factor-adjustment/17040/9)

[https://governance.aave.com/t/arfc-polygon-v2-borrow-rate-adjustments/17252/9](https://governance.aave.com/t/arfc-polygon-v2-borrow-rate-adjustments/17252/9)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xAD6c03BF78A3Ee799b86De5aCE32Bb116eD24637#code#F1#L1)

* Polygon - V2 - [proposal payloads](https://polygonscan.com/address/0x2dbBe7E30CD959A192FeFCEd9A5ae681d540deB4#code#F1#L1)

* Polygon - V3 - [proposal payloads](https://polygonscan.com/address/0xbD8e0Bf17832D0D0dC05168E85eAEAD2b9024E7D#code#F1#L1)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x96cecD5D7A4b740f6a8eF2787fe88E0Bd480d79f/contract/43114/code)

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0xb3f69D75ae2295D68fD9CC9Bc53983781Ee00c10#code#F1#L1)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x22ca2Dd3063189F9E7e76fA3078E2d916B3998b7#code#F1#L1)

* Base - [proposal payloads](https://basescan.org/address/0x6B96B41a531713a141F6EcBbae80715601d0e456#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal suggests reserve factor changes for some assets in Aave V2 and V3 on Ethereum, Polygon, Avalanche, Optimism, Arbitrum and Base as well as variableRateSlope1 changes for some assets in Aave V2 on Polygon.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xa50adaf6e3dd2284ba743cad249b725de857d3d8bd28da780605a008c2282d4f](https://etherscan.io/tx/0xa50adaf6e3dd2284ba743cad249b725de857d3d8bd28da780605a008c2282d4f)

```
- proposalId: 147
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xb47359ccae9af33a6bf55f8e569f990130a806685bbe16e9a613f6ffda34513a
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
      "payloadId": "159" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "77" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "46" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "44" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "46" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "29" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xb47359ccae9af33a6bf55f8e569f990130a806685bbe16e9a613f6ffda34513a" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/147.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/147.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/159.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/159.md)

* Polygon - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/77.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/77.md)

* Avalanche - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/46.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/46.md)

* Optimism - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/44.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/44.md)

* Arbitrum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/46.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/46.md)

* Base - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/29.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/29.md)

<br>

### Technical analysis

We have verified that the payload does the following:

- Changes the reserve factor of USDC.e on Polygon V3, Optimism V3 and Arbitrum V3 as well as USDbC on base V3 to 30%

- Changes the reserve factor of DAI, USDC, USDT and WETH on Ethereum V2 to 65% and the reserve factor of LINK and WBTC on Ethereum V2 to 70%

- Changes the reserve factor of DAIe, USDCe, USDTe, WAVAX and WETHe on Avalanche V2 to 60% and the reserve factor of WBTCe on Avalanche V2 to 65% 

- Changes the variableRateSlope1 for DAI, USDT, wBTC, wETH, wUSDC, wMATIC on Polygon V2 to 12%, 12%, 7%, 7%, 12% and 9% respectively

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
