# Proposal 284. Aave v2 Polygon - Reserve Factor (RF) updates

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=284](https://app.aave.com/governance/proposal/?proposalId=284)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937](https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal adjusts multiple Reserve Factor parameters on Aave v2 Polygon.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x8b0481d977dc20d725a3e19fe62eca5632675c6239b6ef680aa50f619dd525c0](https://etherscan.io/tx/0x8b0481d977dc20d725a3e19fe62eca5632675c6239b6ef680aa50f619dd525c0)

```
- id: 284
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000812ddad273544754d0672a009c27550899e658aa]
- withDelegatecalls: [true]
- startBlock: 17821344
- endBlock: 17840544
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x2e8b4f2a95fd6501e53f0e949f585c33f8a6c7dd884761edceed98ed043b869a
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/284.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/284.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/284_Polygon_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/284_Polygon_pending_0.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://polygonscan.com/address/0x812ddad273544754d0672a009c27550899e658aa#code#F1#L31) does the following changes of Reserve Factors on Aave v2 Polygon, by interacting with its PoolConfigurator smart contract:

*WMATIC*: 41% -> **46%**

*CRV*: 38% -> **99%**

*WBTC*: 55% -> **60%**

*USDC*: 23% -> **28%**

*GHST*: 60% -> **99%**

*LINK*: 50% -> **99%**

*WETH*: 45% -> **50%**

*DAI*: 21% -> **26%**

*BAL*: 32% -> **37%**

*USDT*: 22% -> **27%**


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
