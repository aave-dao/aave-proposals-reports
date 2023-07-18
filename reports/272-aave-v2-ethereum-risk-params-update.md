# Proposal 272. Aave v2 Ethereum - Risk parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=272](https://app.aave.com/governance/proposal/?proposalId=272)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-aave-v2-ethereum-2023-6-23/13789](https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-aave-v2-ethereum-2023-6-23/13789)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal adjusts the LTV, Liquidation Threshold, Liquidation Bonus and Reserve Factor parameters of multiple assets on Aave v2 Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xef2b8c3d32cb5e5a70121b5e18d5ad710cb53e69d586a2045d58239d3bdc75cc](https://etherscan.io/tx/0xef2b8c3d32cb5e5a70121b5e18d5ad710cb53e69d586a2045d58239d3bdc75cc)

```
- id: 272
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x6aec39df2f98915dbaf2e234792696623c591a6d]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17683703
- endBlock: 17702903
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x126cd68c2c9d29f151c8833ee840260ebaa00d7d6ea8f0867c9f719704ca3c12
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/272.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/272.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x6aec39df2f98915dbaf2e234792696623c591a6d#code#F1#L13) does the following changes on Aave v2 Ethereum, but interacting with its PoolConfigurator smart contract:

YFI
- LTV: 50% -> **0%**
- Liquidation Threshold: 65% -> **55%**
- Liquidation Bonus: 7.5% -> **10%**
- Reserve Factor: 20% -> **30%**

BAT
- LTV: 65% -> **0%**
- Liquidation Threshold: 70% -> **52%**
- Liquidation Bonus: 7.5% -> **10%**
- Reserve Factor: 20% -> **30%**

MANA
- LTV: 61.5% -> **0%**
- Liquidation Threshold: 72% -> **62%**
- Liquidation Bonus: 7.5% -> **10%**
- Reserve Factor: 35% -> **45%**

DPI
- LTV: 65% -> **0%**
- Liquidation Threshold: 70% -> **42%**
- Liquidation Bonus: 7.5% -> **10%**
- Reserve Factor: 20% -> **30%**

REN
- LTV: 55% -> **0%**
- Liquidation Threshold: 60% -> **40%**
- Liquidation Bonus: 7.5% -> **10%**
- Reserve Factor: 20% -> **30%**

CVX
- LTV: 35% -> **0%**
- Liquidation Threshold: 45% -> **40%**
- Reserve Factor: 20% -> **30%**

xSUSHI
- LTV: 50% -> **0%**
- Liquidation Threshold: 65% -> **60%**
- Liquidation Bonus: 8.5% -> **10%**
- Reserve Factor: 35% -> **45%**

BAL
- LTV: 65% -> **0%**
- Liquidation Threshold: 70% -> **55%**
- Reserve Factor: 20% -> **30%**

KNC
- LTV: 60% -> **0%**
- Liquidation Threshold: 70% -> **1%**
- Reserve Factor: 35% -> **45%**

ZRX
- LTV: 55% -> **0%**
- Liquidation Threshold: 65% -> **45%**
- Liquidation Bonus: 7.5% -> **10%**
- Reserve Factor: 20% -> **30%**

ENJ
- LTV: 60% -> **0%**
- Liquidation Threshold: 67% -> **60%**
- Liquidation Bonus: 6% -> **10%**
- Reserve Factor: 20% -> **30%**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
