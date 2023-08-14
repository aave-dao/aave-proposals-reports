# Proposal 294. Aave v2 Ethereum - BUSD off-boarding pt 3

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=294](https://app.aave.com/governance/proposal/?proposalId=294)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-busd-offboarding-plan-part-iii/14136](https://governance.aave.com/t/arfc-busd-offboarding-plan-part-iii/14136)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

:money_with_wings: funds-release

<br>

### Context

This proposal proceeds with another phase of the off-boarding of BUSD on Aave v2 Ethereum, by  modifying its interest rate strategy, and withdrawing aBUSD held by the Aave Ethereum Collector to BUSD.

Additionally, the payload does an adjustment on the rate strategy of TUSD, to have a lower stable rate slope 2 (good practises, even if stable borrowing disabled).

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xc37e0ed83eade7f892f956c5c64d6c7d46ec142b638363031f740b2a59d1242b](https://etherscan.io/tx/0xc37e0ed83eade7f892f956c5c64d6c7d46ec142b638363031f740b2a59d1242b)

```
- id: 294
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x40c3aecdeda52375eacccd4f89420ffaa1607e3c]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17885604
- endBlock: 17904804
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xd1bfa4950530040dadfdb171ab4f6dfeb0d96983923f90c21e072427fb566888
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/294.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/294.md)

<br>

### Technical analysis

The [proposal payload](https://etherscan.io/address/0x40c3aecdeda52375eacccd4f89420ffaa1607e3c#code#F1#L16) does the following:

1. Withdraw the current balance of aBUSD (~77'000 BUSD, but can change depending on available liquidity) to BUSD to the Aave Collector, common for Aave v2 and v3. The payload properly checks available liquidity to avoid any kind of revert.

2. Replace the interest rate strategy of BUSD with a new one with the following changes:

- Optimal usage point: 2% -> **1%**
- Base variable rate: 3% -> **100%**
- Variable rate slope 1: 7% -> **70%**
- Stable rate slope 1: 7% -> **70%**
- Stable rate slope 2: 3000% -> **300%**

3. Replace the interest rate strategy of TUSD with a new one with the following changes:

- Stable rate slope 2: 2000% -> **200%**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Multiple payloads used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
