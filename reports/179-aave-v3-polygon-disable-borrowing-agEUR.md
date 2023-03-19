# Proposal 179. Aave v3 Polygon - disable borrowing of agEUR

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=179](https://app.aave.com/governance/proposal/?proposalId=179)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-disable-borrow-of-ageur-on-aave-v3-polygon/12275](https://governance.aave.com/t/arfc-disable-borrow-of-ageur-on-aave-v3-polygon/12275)

<br>

## BGD analysis

<br>

### Proposal types

:ice_cube: freeze-asset (borrowing)

<br>

### Context

Due to the uncertainty about backing of agEUR post-Euler exploit, this proposal disables borrowing of agEUR on Aave v3 Polygon, asset already not enabled as collateral.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x1427daa876b021adea06ac00f330f9a9b330562dc06ab34c52715d8dfebed196](https://etherscan.io/tx/0x1427daa876b021adea06ac00f330f9a9b330562dc06ab34c52715d8dfebed196)

```
- id: 179
- creator: 0xbc540e0729b732fb14afa240aa5a047ae9ba7df0
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x00000000000000000000000060bcd1caf97c3fcbc35bf92a8852728420c34fb5]
- withDelegatecalls: [true]
- startBlock: 16834833
- endBlock: 16854033
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x94cd6fdec271930902d9785b81c337b9895a3edd75555cc4107f6922adff7622
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/179.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/179.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/179_fx_21_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/179_fx_21_0.md)

<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system.

The [proposal payload](https://polygonscan.com/address/0x60bcd1caf97c3fcbc35bf92a8852728420c34fb5#code#F15#L1) simply interacts with the [PoolConfigurator](https://polygonscan.com/address/0x8145eddDf43f50276641b55bd3AD95944510021E) of Aave v3 Polygon to disable borrowing of agEUR, by calling `setReserveBorrowing()`.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
