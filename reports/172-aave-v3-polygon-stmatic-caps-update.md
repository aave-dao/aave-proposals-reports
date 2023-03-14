# Proposal 172. Aave v3 Polygon - update of stMATIC supply cap

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=172](https://app.aave.com/governance/proposal/?proposalId=172)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-increase-stmatic-supply-cap/12038](https://governance.aave.com/t/arfc-increase-stmatic-supply-cap/12038)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the supply cap of stMATIC on Aave v3 Polygon.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x300ffcf556f290d68c7f66616e28c19a77f1bf65f84017fe9fa869700e394d22](https://etherscan.io/tx/0x300ffcf556f290d68c7f66616e28c19a77f1bf65f84017fe9fa869700e394d22)

```
- id: 172
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000aa7ef2f9b31fa26e802ca9b3e33990ada4143fb9]
- withDelegatecalls: [true]
- startBlock: 16783774
- endBlock: 16802974
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x6ec984d91925d4f6c9a9e7bdf06d1ce37823032c5dd7d16c6a8fa55bb4fbe461
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/172.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/172.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/172_fx_17_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/172_fx_17_0.md)

<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Polygon.

The [Polygon payload](https://polygonscan.com/address/0xaa7ef2f9b31fa26e802ca9b3e33990ada4143fb9#code#F15#L1) only updates the stMATIC supply cap from 7'500'000 stMATIC to 15'000'000 stMATIC.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
