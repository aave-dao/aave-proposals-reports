# Proposal 137. Aave v2 Ethereum - Risk Parameter Updates 

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=137](https://app.aave.com/governance/proposal/?proposalId=137)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-risk-parameter-updates-for-aave-v2-ethereum-lt-and-ltv-2022-12-01/10897](https://governance.aave.com/t/arc-risk-parameter-updates-for-aave-v2-ethereum-lt-and-ltv-2022-12-01/10897)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal is an update of risk parameters on Aave v2 Ethereum by Chaos Labs, affecting DAI and USDC.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x0c620dc140f4bade14f61b165509cf0060fa17cc45577adb045ac27e3d92ce67](https://etherscan.io/tx/0x0c620dc140f4bade14f61b165509cf0060fa17cc45577adb045ac27e3d92ce67)

```
- id: 137
- creator: 0xbc540e0729b732fb14afa240aa5a047ae9ba7df0
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xeca5bdf0c2b352cbe2d9a19b555e1ec269d4765c,0x60bcd1caf97c3fcbc35bf92a8852728420c34fb5]
- values: [0,0]
- signatures: [execute(),execute()]
- calldatas: [0x,0x]
- withDelegatecalls: [true,true]
- startBlock: 16235369
- endBlock: 16254569
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x92596c371b9f45caf0389154f37aa9ab679acdf2763c4ece366615345ba14cbf
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/137.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/137.md)

<br>

### Technical analysis

From a technical perspective, we have verified that the proposal payload does the following changes on Aave v2 Ethereum, by interacting with the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code):

1. DAI:
  - LTV: **77% -> 75%**
  - Liquidation Threshold: **90% -> 87%**
2. USDC:
  - LTV: **87% -> 80%**
  - Liquidation Threshold: **89% -> 87.5%**



<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
