# Proposal 334. Aave v2 Polygon - Reserve Factor updates

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=334](https://app.aave.com/governance/proposal/?proposalId=334)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937/7](https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937/7)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal increases the Reserve Factor parameter on multiple Aave v2 Polygon assets, with the objective of incentivising migrations to Aave v3 Polygon.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x4ed6b8c4a40d4f7904e5549cb3cb0eae5252595d3a7c6da8cc40760738d4ba8b](https://etherscan.io/tx/0x4ed6b8c4a40d4f7904e5549cb3cb0eae5252595d3a7c6da8cc40760738d4ba8b)

```
- id: 334
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x0000000000000000000000002120570b9add275864830b173bdaf50b0f4e748a]
- withDelegatecalls: [true]
- startBlock: 18269385
- endBlock: 18288585
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xe12df3fc3a36823ca5acf1443be4ae93ea829bb058c9c6a676b73f29c513d3c2
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/334.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/334.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/334_Polygon_66.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/334_Polygon_66.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://polygonscan.com/address/0x2120570b9add275864830b173bdaf50b0f4e748a#code#F1#L31) properly changes the following Reserve Factors on Aave v2 Polygon:

WMATIC: 51% -> **56%**

WBTC: 65% -> **70%**

USDC: 33% -> **38%**

WETH: 55% -> **60%**

DAI: 31% -> **36%**

BAL: 42% -> **47%**

USDT: 32% -> **37%**


The changes are consistent with those defined on the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
