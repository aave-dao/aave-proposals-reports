# Proposal 136. Aave v2 Ethereum - Risk Parameter Updates 

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=136](https://app.aave.com/governance/proposal/?proposalId=136)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-risk-parameter-updates-for-aave-v2-ethereum-lts-and-ltvs-for-long-tail-assets-2022-12-04/10926](https://governance.aave.com/t/arc-risk-parameter-updates-for-aave-v2-ethereum-lts-and-ltvs-for-long-tail-assets-2022-12-04/10926)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal is an update of risk parameters on Aave v2 Ethereum by Chaos Labs, affecting ENS, MKR, SNX and CRV.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x1c3bb638e359bdcb9e2b82623adbac5eddab8bef20d323721aef19daee666a37](https://etherscan.io/tx/0x1c3bb638e359bdcb9e2b82623adbac5eddab8bef20d323721aef19daee666a37)

```
- id: 136
- creator: 0xbc540e0729b732fb14afa240aa5a047ae9ba7df0
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x33d7385b2bf82b2183afc66dc84ea5f3f2d240d5]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16235304
- endBlock: 16254504
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x31cc3826fed671c95f9522cdac3cb6b6b9bf75ba311c28e84327729586254eed
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/136.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/136.md)

<br>

### Technical analysis

From a technical perspective, we have verified that the proposal payload does the following changes on Aave v2 Ethereum, by interacting with the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code):

1. ENS:
  - LTV: **50% -> 47%**
  - Liquidation Threshold: **60% -> 57%**
2. MKR:
  - LTV: **65% -> 62%**
  - Liquidation Threshold: **70% -> 67%**
3. SNX:
  - LTV: **49% -> 46%**
  - Liquidation Threshold: **65% -> 62%**
4. CRV:
  - LTV: **55% -> 52%**
  - Liquidation Threshold: **61% -> 58%**



<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
