# Proposal 283. Aave v2 Ethereum - FEI risk parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=283](https://app.aave.com/governance/proposal/?proposalId=283)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-fei-on-aave-v2-ethereum-2023-6-22/13782](https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-fei-on-aave-v2-ethereum-2023-6-22/13782)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

:crystal_ball: oracle-addition

<br>

### Context

This proposal adjusts the LTV and Liquidation Threshold on Aave v2 Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x8e214e629447dcb89498491d31c28e5947ec7cdb09b8cd76eb4e90b80e49cfd5](https://etherscan.io/tx/0x8e214e629447dcb89498491d31c28e5947ec7cdb09b8cd76eb4e90b80e49cfd5)

```
- id: 283
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xad491ed5a7fb2214c51333c319842dac833ab08b]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17801258
- endBlock: 17820458
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xb3ed114aabdd26aac46ea46eb45215fe26966f59d77b1fe2643134047f9951cc
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/283.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/283.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xad491ed5a7fb2214c51333c319842dac833ab08b#code#F1#L13) does the following changes on Aave v2 Ethereum, by interacting with its PoolConfigurator smart contract:

FEI
- LTV: 65% -> **0%**
- Liquidation Threshold: 75% -> **1%**
- Liquidation Bonus: 6.5% -> **10%**

Additionally, following the rationale [HERE](https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-fei-on-aave-v2-ethereum-2023-6-22/13782/3), the FEI price feed is replaced with an [ad-hoc adapter pricing FEI at 0.95$](https://etherscan.io/address/0xac3AF0f4A52C577Cc2C241dF51a01FDe3D06D93B#code#F1#L13) (with ETH reference, respecting the requirements of Aave v2 Ethereum).

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
