# Proposal 289. Treasury Management - swap USDT from treasury to aCRV

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=289](https://app.aave.com/governance/proposal/?proposalId=289)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-acquire-crv-with-treasury-usdt/14251](https://governance.aave.com/t/arfc-acquire-crv-with-treasury-usdt/14251)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposal executes a first-of-its-kind swap of USDT from the Aave Ethereum Collector to aCRV, which the USDT atomically used to repay debt of USDT of address `0x7a16ff8270133f063aab6c9977183d9e72835428`.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xd4dc1d9b257f8f048ad37ebf455d511b86b9ae67720fc175f837fd8d42e353bd](https://etherscan.io/tx/0xd4dc1d9b257f8f048ad37ebf455d511b86b9ae67720fc175f837fd8d42e353bd)

```
- id: 289
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x8eda0756f0d7dffc8488a19cf3b949bebd132191]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17871434
- endBlock: 17890634
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x03621fdd5b0f4431c88e43b154b7192c0dd0ab0c0cbecb2d6336c49a2a6bcc54
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/289.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/289.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x8eda0756f0d7dffc8488a19cf3b949bebd132191#code#F1#L14) does the following:

1. Transfer from the [counterparty address](https://etherscan.io/address/0x7a16ff8270133f063aab6c9977183d9e72835428) 5'000'000 aCRV, to the Aave Ethereum Collector.
This will depend on the counterparty having given approval in advance to the Aave Governance Level 1 Executor (Short Executor).

2. Use 2'000'000 USDT from the Aave Ethereum Collector to repay same value of debt of behalf the counterparty address, with ~20'100'000 USDT outstanding borrowings at the moment.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
