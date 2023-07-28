# Proposal 277. Aave v3 Ethereum, Arbitrum and Aave v2 Ethereum - Risk parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=277](https://app.aave.com/governance/proposal/?proposalId=277)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-gauntlet-risk-parameter-updates-for-ethereum-v3-arbitrum-v3-ethereum-v2-2023-06-26/13825](https://governance.aave.com/t/arfc-gauntlet-risk-parameter-updates-for-ethereum-v3-arbitrum-v3-ethereum-v2-2023-06-26/13825)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal adjusts the LTV, Liquidation Threshold, Liquidation Bonus of different assets across Aave v3 Ethereum, Arbitrum and Aave v2 Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x16da7de09edbf8939213b3b2af38f7509f5a8eac5de43dc06360a67230a5d615](https://etherscan.io/tx/0x16da7de09edbf8939213b3b2af38f7509f5a8eac5de43dc06360a67230a5d615)

```
- id: 277
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xd1b3e25fd7c8ae7caddc6f71b461b79cd4ddcfa3,0x0c9c38cb9480b86c1f624613749b02379b0448ce,0xf7c3350757de224bdb2b77a3943c8667acee3d37]
- values: [0,0,0]
- signatures: [execute(address),execute(),execute()]
- calldatas: [0x000000000000000000000000ac63290bc16fbc33353b14f139cef1c660ba56f0,0x,0x]
- withDelegatecalls: [true,true,true]
- startBlock: 17778020
- endBlock: 17797220
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xfb32092f0cf0b1cb3a3bac4df98bcfd955a4afe3c96a2e1e17241f3bab823a2f
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/277.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/277.md)


**Arbitrum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/277_Arbitrum_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/277_Arbitrum_pending_0.md)

<br>

### Technical analysis

We have verified the proposal properly uses cross-chain governance (Arbitrum), the BGD Aave Config Engine (v3 Ethereum) and the Aave v2 PoolConfigurator (v2 Ethereum) to do the following changes on 3 separate payloads:

[Aave v3 Ethereum](https://etherscan.io/address/0x0c9c38cb9480b86c1f624613749b02379b0448ce#code#F1#L35)

DAI
- LTV: 67% -> **77%**

USDC
- Liquidation Threshold: 79% -> **80%**

wstETH
- Liquidation Bonus: 7% -> **6%**

[Aave v2 Ethereum](https://etherscan.io/address/0xf7c3350757de224bdb2b77a3943c8667acee3d37#code#F1#L73)

SNX
- Liquidation Threshold: 62% -> **59%**


[Aave v3 Arbitrum](https://arbiscan.io/address/0xac63290bc16fbc33353b14f139cef1c660ba56f0#code#F1#L17)

LINK
- Liquidation Threshold: 75% -> **77.5%**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:?: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:x: BGD reviewed the procedure followed to submit the proposal.
