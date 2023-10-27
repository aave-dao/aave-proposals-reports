# Proposal 353. Aave v2 Polygon - Reserve Factor updates

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=353](https://app.aave.com/governance/proposal/?proposalId=353)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937/8](https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937/8)

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

Transaction: [https://etherscan.io/tx/0x24d537c711d64de8e0bc3b86aae029c48b817a78b5d1715b330a010b8e1dcd15](https://etherscan.io/tx/0x24d537c711d64de8e0bc3b86aae029c48b817a78b5d1715b330a010b8e1dcd15)

```
- id: 353
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x00000000000000000000000053af3e66dfd8182f1084d8f36d4c1085a3962b7a]
- withDelegatecalls: [true]
- startBlock: 18421130
- endBlock: 18440330
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x7660944ede5190c84a6fb96925cdae82a269bff787c407d8f903f4d4db5fead5
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/353.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/353.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/353_Polygon_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/353_Polygon_pending_0.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://polygonscan.com/address/0x53af3e66dfd8182f1084d8f36d4c1085a3962b7a#code#F1#L13) properly changes the following Reserve Factors on Aave v2 Polygon:

WMATIC: 56% -> **61%**

WBTC: 70% -> **75%**

USDC: 38% -> **43%**

WETH: 60% -> **65%**

DAI: 36% -> **41%**

BAL: 47% -> **52%**

USDT: 37% -> **42%**


The changes are consistent with those defined on the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
