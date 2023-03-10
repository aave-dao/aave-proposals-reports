# Proposal 171. Aave v3 Arbitrum - Risk params update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=171](https://app.aave.com/governance/proposal/?proposalId=171)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-chaos-labs-risk-parameter-updates-aave-v3-arbitrum-2023-02-20/11986](https://governance.aave.com/t/arc-chaos-labs-risk-parameter-updates-aave-v3-arbitrum-2023-02-20/11986)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the risk parameters of WETH, WBTC, DAI and USDC on Aave v3 Arbitrum.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x3ed0dcc41714a3310dbda2879d4124f8bd7d052ddb44f4273dc9807ccdbbc95d](https://etherscan.io/tx/0x3ed0dcc41714a3310dbda2879d4124f8bd7d052ddb44f4273dc9807ccdbbc95d)

```
- id: 171
- creator: 0xbc540e0729b732fb14afa240aa5a047ae9ba7df0
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x2e2b1f112c4d79a9d22464f0d345de9b792705f1]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x0000000000000000000000003a4f2a6c7e1e641afad6300553a0bb82d6c46a2e]
- withDelegatecalls: [true]
- startBlock: 16777429
- endBlock: 16796629
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x252c583ff5fb8dfb72ac79e8fe044eb82d4adc2a431e0f7c69b692c34b563b84
```

<br>

### Aave Seatbelt reports

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/171.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/171.md)


**Arbitrum**

Aave Seatbelt doesn't support Arbitrum yet.


<br>

### Technical analysis

From a technical perspective, we have verified the [proposal payload](https://arbiscan.io/address/0x3a4f2a6c7e1e641afad6300553a0bb82d6c46a2e#code#F15#L1) changes the following risk parameters by interacting with the [PoolConfigurator of Aave v3 Arbitrum](https://arbiscan.io/address/0x8145eddDf43f50276641b55bd3AD95944510021E):

- WETH:
  - LTV: 80% -> **82.5%**
  - Liquidation Threshold: 82.5% -> **85%**
- WBTC:
  - LTV: 70% -> **73%**
  - Liquidation Threshold: 75% -> **78%**
  - Liquidation Bonus: 10% -> **7%**
- DAI:
  - LTV: 75% -> **77%**
  - Liquidation Threshold: 80% -> **82**
- USDC:
  - LTV: 80% -> **81%**
  - Liquidation Threshold: 85% -> **86%**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
