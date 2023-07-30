# Proposal 280. Aave v2 Ethereum - CRV risk parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=280](https://app.aave.com/governance/proposal/?proposalId=280)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-crv-aave-v2-ethereum-2023-07-10/13952](https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-crv-aave-v2-ethereum-2023-07-10/13952)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal adjusts the LTV and Liquidation Threshold on Aave v2 Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x02c9073874234223f74e7e45b56e4f997413b5cb36b7bcddc1ada40e840b38c2](https://etherscan.io/tx/0x02c9073874234223f74e7e45b56e4f997413b5cb36b7bcddc1ada40e840b38c2)

```
- id: 280
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x2dcbc45d1aa88c1f6f8138ed5e93c8a9a20f5350]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17783645
- endBlock: 17802845
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xd76a03c6d1fac5c9e957bb741f3b13f75ba0682ed4d5d19cca641b44be0e8c62
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/280.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/280.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x2dcbc45d1aa88c1f6f8138ed5e93c8a9a20f5350#code#F1#L13) does the following changes on Aave v2 Ethereum, by interacting with its PoolConfigurator smart contract:

CRV
- LTV: 49% -> **43%**
- Liquidation Threshold: 55% -> **49%**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
