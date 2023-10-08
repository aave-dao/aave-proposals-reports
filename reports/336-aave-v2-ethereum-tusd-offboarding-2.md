# Proposal 336. Aave v2 Ethereum - TUSD off-boarding Part 2

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=336](https://app.aave.com/governance/proposal/?proposalId=336)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-tusd-offboarding-plan-part-ii/14863](https://governance.aave.com/t/arfc-tusd-offboarding-plan-part-ii/14863)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal proceeds with some progressive steps of off-boarding of TUSD from on Aave v2 Ethereum, by modifying its rate strategy and different risk parameters.

Additionally, it includes redeeming TUSD and BUSD to the Aave Ethereum Collector, from Aave v2 Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x9087b93d1467900ef8bef7af8f5e50d9e8e749722b97038883677987dd1e6279](https://etherscan.io/tx/0x9087b93d1467900ef8bef7af8f5e50d9e8e749722b97038883677987dd1e6279)

```
- id: 336
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xd2e9a4c8527dafa273a7fe225f6c40f3b38db1bb]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 18292469
- endBlock: 18311669
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x4ad596694ebb54b87b603a0dc98850e11bd412b3f29d1f8531d53492aa08741f
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/336.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/336.md)

<br>

### Technical analysis

The [proposal payload](https://etherscan.io/address/0xd2e9a4c8527dafa273a7fe225f6c40f3b38db1bb#code#F1#L15) does the following:

1. Changes the following risk parameters of TUSD on Aave v2 Ethereum, by interacting with its PoolConfigurator:

- Liquidation Threshold: 75% -> **65%**
- Reserve Factor: 95% -> **99.9%**

2. Withdraws the current balance of aTUSD (~263'000 aTUSD, but can change depending on available liquidity) to TUSD to the Aave Collector, common for Aave v2 and v3. The payload properly checks available liquidity to avoid any kind of revert.
Same procedure is done with aBUSD, for an approximate amount of ~110'000 aBUSD.

3. Replace the interest rate strategy with a new one with the following changes:

- Optimal usage point: 20% -> **1%**
- Base variable rate: 3% -> **100%**
- Variable rate slope 1: 7% -> **70%**
- Variable rate slope 2: 200% -> **300%**
- Stable rate slope 1: 7% -> **70%**
- Stable rate slope 2: 200% -> **300%**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Multiple payloads used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
