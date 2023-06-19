# Proposal 247. Aave v3 Ethereum - risk parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=247](https://app.aave.com/governance/proposal/?proposalId=247)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-aave-v3-ethereum-2023-05-18/13128](https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-aave-v3-ethereum-2023-05-18/13128)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates multiple risk parameters on Aave v3 Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x434259699e010f2687d47b970f2c757e8a0f677c3e915dbd0bd9600044c32ceb](https://etherscan.io/tx/0x434259699e010f2687d47b970f2c757e8a0f677c3e915dbd0bd9600044c32ceb)

```
- id: 247
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xfa6481b09c273d17701fb90427d6658a028edc18]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17491464
- endBlock: 17510664
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x169718719612fd6abd2fe3361fb879b2ad8087d4e00b9c9c3449dc9d2474f62a
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/247.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/247.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xfa6481b09c273d17701fb90427d6658a028edc18#code#F1#L11) does the following changes by interacting with the BGD Aave v3 Ethereum Config Engine:

WETH:
- LTV: 80% -> **80.5%**
- Liquidation Threshold: 82.5% -> **83%**

WBTC
- LTV: 70% -> **73%**
- Liquidation Threshold: 75% -> **78%**
- Liquidation Bonus: 6.25% -> **5%**

DAI:
- LTV: 64% -> **67%**
- Liquidation Threshold: 77% -> **80%**

USDC:
- LTV: 74% -> **77%**
- Liquidation Threshold: 76% -> **79%**

LINK:
- LTV: 50% -> **53%**
- Liquidation Threshold: 65% -> **68%**
- Liquidation Bonus: 7.5% -> **7%**

wstETH:
- LTV: 68.5% -> **69%**
- Liquidation Threshold: 79.5% -> **80%**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
