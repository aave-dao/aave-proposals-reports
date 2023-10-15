# Proposal 341. Aave v2 Ethereum - Risk parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=341](https://app.aave.com/governance/proposal/?proposalId=341)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-v2-ethereum-deprecation-10-03-2023/15040](https://governance.aave.com/t/arfc-v2-ethereum-deprecation-10-03-2023/15040)

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

Transaction: [https://etherscan.io/tx/0x3d8b00c1027f20757d851066d623f2eda320e0a034cff5fb1a31cb54caa2f33d](https://etherscan.io/tx/0x3d8b00c1027f20757d851066d623f2eda320e0a034cff5fb1a31cb54caa2f33d)

```
- id: 341
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xff374ad1be52ff54cf576586253a113d3f48d4b7]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 18333191
- endBlock: 18352391
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x6df1ac73c6175c6e3a3cb8b8953739452c9024d895ccca20ecf151161eb39d8e
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/341.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/341.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xff374ad1be52ff54cf576586253a113d3f48d4b7#code#F1#L13) updates the following parameters on Aave v2 Ethereum, via its Pool Configurator contract:

YFI
- Liquidation Threshold: 50% -> **45%**

BAT
- Liquidation Threshold: 40% -> **1%**

MANA
- Liquidation Threshold: 54% -> **48%**

1INCH
- Liquidation Threshold: 40% -> **24%**
- LTV: 30% -> **0%**

DPI:
- Liquidation threshold: 42% -> **16%**

UNI
- LTV: 58% -> **0%**

REN
- Liquidation Threshold: 32% -> **27%**

CVX
- Liquidation Threshold: 35% -> **33%**

LINK:
- LTV: 70% -> **0%**
- Liquidation Threshold: 83% -> **82%**

XSUSHI
- Liquidation Threshold: 57% -> **28%**

MKR
- Liquidation Threshold: 50% -> **35%**
- LTV: 45% -> **0%**

BAL
- Liquidation Threshold: 35% -> **25%**

SNX
- Liquidation Threshold: 49% -> **43%**
- LTV: 36% -> **0%**

ENS
- Liquidation Threshold: 52% -> **50%**
- LTV: 42% -> **0%**

CRV:
- Reserve Factor: 45% -> **42%**

ZRX
- Liquidation Threshold: 42% -> **37%**

ENJ
- Liquidation Threshold: 52% -> **50%**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
