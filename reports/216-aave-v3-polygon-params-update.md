# Proposal 216. Aave v3 Polygon - risk parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=216](https://app.aave.com/governance/proposal/?proposalId=216)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-aave-v3-polygon-2023-04-23/12828/2](https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-aave-v3-polygon-2023-04-23/12828/2)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates multiple risk parameters on Aave v3 Polygon.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xb9ba0f685061e33747cd8f62b0edb5c2399883f9f3c0efc92e6e5a754c9f1f52](https://etherscan.io/tx/0xb9ba0f685061e33747cd8f62b0edb5c2399883f9f3c0efc92e6e5a754c9f1f52)

```
- id: 216
- creator: 0xbc540e0729b732fb14afa240aa5a047ae9ba7df0
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000c53586aa2626094bd33c123794e34417ea877a36]
- withDelegatecalls: [true]
- startBlock: 17193612
- endBlock: 17212812
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x0534109ab793da6816093b041e5f1685ed1f2523ad69c7e734a85a5bcf22895b
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/b83e74938fced0f827b0238dfeb15659bd5d04da/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/216.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/b83e74938fced0f827b0238dfeb15659bd5d04da/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/216.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/b83e74938fced0f827b0238dfeb15659bd5d04da/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/216_fx_1683558613_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/b83e74938fced0f827b0238dfeb15659bd5d04da/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/216_fx_1683558613_0.md)


<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Polygon.

The [proposal payload on Polygon](https://polygonscan.com/address/0xc53586aa2626094bd33c123794e34417ea877a36#code#F22#L1) does the following:

WBTC
- LTV: 70% -> **73%**
- Liquidation Threshold: 75% -> **78%**

DAI:
- LTV: 75% -> **76%**
- Liquidation Threshold: 80% -> **81%**

LINK:
- LTV: 50% -> **53%**
- Liquidation Threshold: 65% -> **68%**

WMATIC:
- LTV: 65% -> **68%**
- Liquidation Threshold: 70% -> **73%**
- Liquidation Bonus: 10% -> **7%**


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
