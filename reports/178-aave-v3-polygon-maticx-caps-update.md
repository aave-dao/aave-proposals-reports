# Proposal 178. Aave v3 Polygon - update MATICX supply cap

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=178](https://app.aave.com/governance/proposal/?proposalId=178)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-maticx-supplycap-increase-polygon-v3/12217](https://governance.aave.com/t/arfc-maticx-supplycap-increase-polygon-v3/12217)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal increases the supply cap of MATICX on Aave v3 Polygon.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x16d29b8eedbaac4046152a00ede4571fd4402ee0f4caa3242940b84cf7f2a8cf](https://etherscan.io/tx/0x16d29b8eedbaac4046152a00ede4571fd4402ee0f4caa3242940b84cf7f2a8cf)

```
- id: 178
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x0000000000000000000000006b5af634e20eaa5fc85f9943913aa46a088ac29e]
- withDelegatecalls: [true]
- startBlock: 16834739
- endBlock: 16853939
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x3e8bc6a263be31e0fe385a4420cc03c2a1fd067ad644a55f43e9825039d7a51e
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/178.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/178.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/178_fx_22_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/178_fx_22_0.md)

<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system.

The [proposal payload](https://polygonscan.com/address/0x6b5af634e20eaa5fc85f9943913aa46a088ac29e#code#F15#L1) simply interacts with the [PoolConfigurator](https://polygonscan.com/address/0x8145eddDf43f50276641b55bd3AD95944510021E) of Aave v3 Polygon to update the supply cap of MATICX from 8'600'000 MATICX to 17'200'000 MATIC by calling the `setSupplyCap()` function.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
