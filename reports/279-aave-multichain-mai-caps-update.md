# Proposal 279. Aave v3 Polygon, Arbitrum, Optimism - MAI caps update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=279](https://app.aave.com/governance/proposal/?proposalId=279)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-mai-on-aave-v3-2023-7-23/14110](https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-mai-on-aave-v3-2023-7-23/14110)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal adjusts the supply and borrow caps, together with debt ceilings of the MAI asset on Aave v3 Polygon, Arbitrum and Optimism.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xc0ebabc6167e4d5869d742eb7838b2a29721bdedd21c7efde05e747d38cd63a6](https://etherscan.io/tx/0xc0ebabc6167e4d5869d742eb7838b2a29721bdedd21c7efde05e747d38cd63a6)

```
- id: 279
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b,0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711,0xd1b3e25fd7c8ae7caddc6f71b461b79cd4ddcfa3]
- values: [0,0,0]
- signatures: [execute(address),execute(address),execute(address)]
- calldatas: [0x0000000000000000000000004449a4d0c1ca7c0ea218f11c8a84dd9b8e633d43,0x0000000000000000000000007e840cffea2d273ed58e7b9b806cd8bed619ca88,0x0000000000000000000000004449a4d0c1ca7c0ea218f11c8a84dd9b8e633d43]
- withDelegatecalls: [true,true,true]
- startBlock: 17783518
- endBlock: 17802718
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xf468feb7f05233adbc199ecc411784e9be2501789a76025177b9d5e9ef4b776f
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/279.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/279.md)


**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/279_Polygon_pending_1.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/279_Polygon_pending_1.md)

**Optimism**
[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/279_Optimism_pending_2.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/279_Optimism_pending_2.md)

**Arbitrum**
[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/279_Arbitrum_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/279_Arbitrum_pending_0.md)

<br>

### Technical analysis

We have verified the proposal properly uses cross-chain governance and the BGD Aave Config Engine across the different networks to do the following changes on 3 separate payloads:

[Aave v3 Polygon](https://polygonscan.com/address/0x4449a4d0c1ca7c0ea218f11c8a84dd9b8e633d43#code#F1#L13)

- Supply cap: 2'200'000 MAI -> **900'000 MAI**
- Borrow cap: 1'200'000 MAI -> **700'000 MAI**
- Debt ceiling: 2'000'000 USD -> **180'000 USD**

[Aave v3 Optimism](https://optimistic.etherscan.io/address/0x7e840cffea2d273ed58e7b9b806cd8bed619ca88#code#F1#L13)

- Supply cap: 7'600'000 MAI -> **650'000 MAI**
- Borrow cap: 2'500'000 MAI -> **525'000 MAI**
- Debt ceiling: 1'900'000 USD -> **130'000 USD**

[Aave v3 Arbitrum](https://arbiscan.io/address/0x4449a4d0c1ca7c0ea218f11c8a84dd9b8e633d43#code#F1#L13)

- Supply cap: 4'800'000 MAI -> **325'000 MAI**
- Borrow cap: 2'400'000 MAI -> **250'000 MAI**
- Debt ceiling: 1'200'000 USD -> **100'000 USD**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.