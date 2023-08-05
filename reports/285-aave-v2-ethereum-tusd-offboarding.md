# Proposal 285. Aave v2 Ethereum - TUSD off-boarding

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=285](https://app.aave.com/governance/proposal/?proposalId=285)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-tusd-offboarding-plan/14008](https://governance.aave.com/t/arfc-tusd-offboarding-plan/14008)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal proceeds with some progressive steps of off-boarding of TUSD from on Aave v2 Ethereum, by modifying its rate strategy and different parameters.
In addition, it withdraws aTUSD held by the Aave Ethereum Collector to TUSD. 

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x8c8c6b3a90b11d5db01d79703ec124af9491755518a3aed2bb7ef8911e278d19](https://etherscan.io/tx/0x8c8c6b3a90b11d5db01d79703ec124af9491755518a3aed2bb7ef8911e278d19)

```
- id: 285
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xd44a556eceff5fff13cf0671f51e649d1fa572ac]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17827490
- endBlock: 17846690
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xe9c7824ff7cba1ed5d9c14b1aafb18349bb2cbefab9ef1c7d290a14c2b69b8fc
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/285.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/285.md)

<br>

### Technical analysis

The [proposal payload](https://etherscan.io/address/0xd44a556eceff5fff13cf0671f51e649d1fa572ac#code#F1#L13) does the following:

1. Changes the following risk parameters of TUSD on Aave v2 Ethereum, by interacting with its PoolConfigurator:

- LTV: 75% -> **0%**
- Liquidation Threshold: 77.5% -> **75%**
- Liquidation Bonus: 5% -> **10**
- Reserve Factor: 10% -> **95%**

2. Disables borrowing of TUSD, both variable and stable.

3. Withdraws the current balance of aTUSD (~36'000 aTUSD, but can change depending on available liquidity) to TUSD to the Aave Collector, common for Aave v2 and v3. The payload properly checks available liquidity to avoid any kind of revert.

4. Replace the interest rate strategy with a new one with the following changes:

- Optimal usage point: 80% -> **20%**
- Base variable rate: 0% -> **3%**
- Variable rate slope 1: 4% -> **7%**
- Variable rate slope 2: 100% -> **200%**
- Stable rate slope 1: 2% -> **7%**
- Stable rate slope 2: 100% -> **2000%**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Multiple payloads used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
