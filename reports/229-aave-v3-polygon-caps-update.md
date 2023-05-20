# Proposal 229 (repetition of part of 220). Aave v3 Polygon - Caps update


<br>


### Voting link

[https://app.aave.com/governance/proposal/?proposalId=229](https://app.aave.com/governance/proposal/?proposalId=229)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-maticx-supply-cap-increase-polygon-v3/12657](https://governance.aave.com/t/arfc-maticx-supply-cap-increase-polygon-v3/12657)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the supply cap of MATICX on Aave v3 Polygon.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xafa809c56be6820b25d3953f82f63882a02fd0497b455a4ef071975f48c45cc4](https://etherscan.io/tx/0xafa809c56be6820b25d3953f82f63882a02fd0497b455a4ef071975f48c45cc4)

```
- id: 229
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x00000000000000000000000022c669eedf6e58de81777692b070cdb7432a4f84]
- withDelegatecalls: [true]
- startBlock: 17279544
- endBlock: 17298744
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x590795d20a5b17ad8e144a1e2c61a7c5d2ff8ff2251868d94740def1f9b86eee
```

<br>

### Aave Seatbelt reports

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/229.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/229.md)


**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/229_fx_39_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/229_fx_39_0.md)


<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system for the payload interacting with Polygon.

Regarding the changes, we verified the [proposal payload](https://polygonscan.com/address/0x22c669eedf6e58de81777692b070cdb7432a4f84#code#F23#L13) correctly updates the supply cap of MATICX from 17'200'000 MATIC to **29'300'000 MATICX**.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
