# Proposal 312. Aave v2 Polygon - Reserve Factor updates

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=312](https://app.aave.com/governance/proposal/?proposalId=312)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937/6](https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937/6)

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

Transaction: [https://etherscan.io/tx/0xf213652215a58936fcc879cdd68d084d26c6f30cd0e2706f2d108fd141fdd71e](https://etherscan.io/tx/0xf213652215a58936fcc879cdd68d084d26c6f30cd0e2706f2d108fd141fdd71e)

```
- id: 312
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x00000000000000000000000040fa5610f17a99d20bd428810bec965fe4694238]
- withDelegatecalls: [true]
- startBlock: 18072152
- endBlock: 18091352
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xf71f0e688f22dc80cf6a885c73f929208c305cb0e3c26605930792469439cd8c
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/312.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/312.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/312_Polygon_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/312_Polygon_pending_0.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://polygonscan.com/address/0x40fa5610f17a99d20bd428810bec965fe4694238#code#F1#L31) properly changes the following Reserve Factors on Aave v2 Polygon:

WMATIC: 46% -> **51%**

WBTC: 60% -> **65%**

USDC: 28% -> **33%**

WETH: 50% -> **55%**

DAI: 26% -> **31%**

BAL: 37% -> **42%**

USDT: 27% -> **32%**


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
