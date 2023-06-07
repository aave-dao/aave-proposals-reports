# Proposal 237. Aave v2 Ethereum - BUSD off-boarding pt 2

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=236](https://app.aave.com/governance/proposal/?proposalId=236)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-busd-offboarding-plan-part-ii/13048](https://governance.aave.com/t/arfc-busd-offboarding-plan-part-ii/13048)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

:money_with_wings: funds-release

<br>

### Context

This proposal proceeds with another phase of the off-boarding of BUSD on Aave v2 Ethereum, by modifying its rate strategy and withdrawing the aBUSD held by the Collector to BUSD.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xe1eb60141520672a09481f7e602fab6f62f20de26e3ac9dffd0ac2bdf6027da9](https://etherscan.io/tx/0xe1eb60141520672a09481f7e602fab6f62f20de26e3ac9dffd0ac2bdf6027da9)

```
- id: 237
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x15e4c34a4a3cd147856cc6a293e25ea5385ec23e]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17420650
- endBlock: 17439850
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x682d51cb497c3e479740500d2f8cf128996a1301192c59d68bf7d69000d7ca46
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/237.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/237.md)

<br>

### Technical analysis

The [proposal payload](https://etherscan.io/address/0x15e4c34a4a3cd147856cc6a293e25ea5385ec23e#code#F1#L14) does the following:

1. Replace the interest rate strategy with a new one with the following changes:

- Optimal usage point: 20% -> **2%**
- Variable rate slope 2: 200% -> **300%**
- Stable rate slope 2: 2000% -> **3000%**

2. Withdraw the current balance of aBUSD (~300'000 BUSD, but can change depending on available liquidity) to BUSD to the Aave Collector, common for Aave v2 and v3. The payload properly checks available liquidity to avoid any kind of revert.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Multiple payloads used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
