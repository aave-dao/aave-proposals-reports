# Proposal 303. Treasury Management - Polygon aToken v2 -> v3 migration

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=303](https://app.aave.com/governance/proposal/?proposalId=303)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-migrate-consolidate-polygon-treasury/12248](https://governance.aave.com/t/arfc-migrate-consolidate-polygon-treasury/12248)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposal consolidates treasury assets into the Aave v3 Collector, by migrating from aTokens from Aave v2 Polygon to v3.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x724617ffd29a87aad390de9130df47d91e7e0f6b601b44b40531ca3c5ea53b6d](https://etherscan.io/tx/0x724617ffd29a87aad390de9130df47d91e7e0f6b601b44b40531ca3c5ea53b6d)

```
- id: 303
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000c34a9391c08b64c4a9167d9e1e884b3735ce21b0]
- withDelegatecalls: [true]
- startBlock: 17978196
- endBlock: 17997396
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x29b067e7a40655570b2ef0b52a4f3fe3259460ea62a33ac07cff9e30a0fb58f9
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/303.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/303.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/303_Polygon_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/303_Polygon_pending_0.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://polygonscan.com/address/0xc34a9391c08b64c4a9167d9e1e884b3735ce21b0#code#F1#L35) properly migrates a list of 10 Aave v2 Polygon aTokens (aDAI, aUSDC, aUSDT, aWBTC, aWETH, aWMATIC, aBAL, aCRV, aGHST and aLINK) to their v3 version, by doing the following:

1. First, the payload withdraws the aTokens from the Aave Polygon Collector.
2. The payload approves the BGD v2->v3 Migration Helper contract to use the v2 aTokens.
3. The migration v2->v3 is done, by calling `migrate()` on the Migrator Helper.
4. The resultant Aave v3 Polygon aTokens are deposited into the Aave Polygon Collector.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
