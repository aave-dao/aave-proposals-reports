# Proposal 315. Aave v2 Ethereum - Risk parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=315](https://app.aave.com/governance/proposal/?proposalId=315)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-aave-v2-ethereum-2023-08-09/14404](https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-aave-v2-ethereum-2023-08-09/14404)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates multiple risk parameters on Aave v2 Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x0d5f8b535b74ab05bc6f1f4be237a6cec391ba566a15ce2572f4a90d6cb9b54a](https://etherscan.io/tx/0x0d5f8b535b74ab05bc6f1f4be237a6cec391ba566a15ce2572f4a90d6cb9b54a)

```
- id: 315
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x4094b97422dc9423e6e1bdd6bc540e80ab053a6b]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 18085657
- endBlock: 18104857
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x62072da4710055d1fd7be0bfe3b4c4a51d7669e3dea76ed1f3fdb26f54a032c7
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/315.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/315.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x4094b97422dc9423e6e1bdd6bc540e80ab053a6b#code#F1#L13) updates the following parameters on Aave v2 Ethereum, via its Pool Configurator contract:

GUSD:
- Reserve Factor: 15% -> **20%**

YFI
- Reserve Factor: 30% -> **35%**
- Liquidation Threshold: 55% -> **50%**

BAT
- Reserve Factor: 30% -> **35%**
- Liquidation Threshold: 52% -> **40%**

MANA
- Reserve Factor: 45% -> **50%**
- Liquidation Threshold: 62% -> **54%**

1INCH
- Reserve Factor: 25% -> **30%**
- Liquidation Threshold: 50% -> **40%**
- LTV: 40% -> **30%**

DPI:
- Reserve Factor: 30% -> **35%**

UNI
- Reserve Factor: 25% -> **30%**
- Liquidation Threshold: 77% -> **70%**
- LTV: 65% -> **58%**

WBTC:
- Reserve Factor: 25% -> **30%**

REN
- Reserve Factor: 30% -> **35%**
- Liquidation Threshold: 40% -> **32%**

CVX
- Reserve Factor: 30% -> **35%**
- Liquidation Threshold: 40% -> **35%**

LINK:
- Reserve Factor: 25% -> **30%**

SUSD:
- Reserve Factor: 25% -> **30%**

LUSD:
- Reserve Factor: 15% -> **20%**

FRAX:
- Reserve Factor: 25% -> **30%**

XSUSHI
- Reserve Factor: 45% -> **50%**
- Liquidation Threshold: 60% -> **57%**

USDP:
- Reserve Factor: 15% -> **20%**

MKR
- Reserve Factor: 25% -> **30%**
- Liquidation Threshold: 64% -> **50%**
- LTV: 59% -> **45%**

USDC:
- Reserve Factor: 15% -> **20%**

BAL
- Reserve Factor: 30% -> **35%**
- Liquidation Threshold: 55% -> **35%**

SNX
- Reserve Factor: 40% -> **45%**
- Liquidation Threshold: 59% -> **49%**
- LTV: 46% -> **36%**

WETH:
- Reserve Factor: 20% -> **25%**

ENS
- Reserve Factor: 25% -> **30%**
- Liquidation Threshold: 57% -> **52%**
- LTV: 47% -> **42%**

CRV:
- Reserve Factor: 25% -> **30%**

USDT:
- Reserve Factor: 15% -> **20%**

ZRX
- Reserve Factor: 30% -> **35%**
- Liquidation Threshold: 45% -> **42%**

ENJ
- Reserve Factor: 30% -> **35%**
- Liquidation Threshold: 60% -> **52%**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
