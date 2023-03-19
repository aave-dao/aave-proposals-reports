# Proposal 177. Aave v3 Polygon - GHST parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=177](https://app.aave.com/governance/proposal/?proposalId=177)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-ghst-polygon-v3-soft-freeze/12192](https://governance.aave.com/t/arfc-ghst-polygon-v3-soft-freeze/12192)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

Due to an important change on the dynamics of liquidity of GHST, this proposal changes its risk parameters on Aave v3 Polygon, to effectively "freeze" the exposure of the protocol on the current state, setting LTV to 0, supply and borrow caps to current levels and disabling borrowing.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x29d64110e75dda84d62601fccb36ab6bcad9b182350042943c731c6350ddfe3c](https://etherscan.io/tx/0x29d64110e75dda84d62601fccb36ab6bcad9b182350042943c731c6350ddfe3c)

```
- id: 177
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000a0a864d3b0837e4806a91647c6ad382a7f73e1a8]
- withDelegatecalls: [true]
- startBlock: 16800630
- endBlock: 16819830
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xe6be54663d94d7012909b7237da14661be98e50a773fa4b6c724c8ee966872dd
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/177.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/177.md)

**Polygon**
[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/177_fx_17_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/177_fx_17_0.md)

<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system.

The [proposal payload](https://polygonscan.com/address/0xa0a864d3b0837e4806a91647c6ad382a7f73e1a8#code#F15#L1) does the following:

- Sets supply cap of GHST to 4'650'000 GHST.
- Sets GHST borrow cap to 220'000 GHST.
- Sets LTV of GHST to 0.
- Disables borrowing of GHST.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
