# Proposal 339. Aave v3 Polygon - stMATIC/MATICx risk parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=339](https://app.aave.com/governance/proposal/?proposalId=339)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-gauntlet-recommendation-to-lower-stmatic-maticx-non-emode-lt/14859](https://governance.aave.com/t/arfc-gauntlet-recommendation-to-lower-stmatic-maticx-non-emode-lt/14859)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal reduces the Liquidation Threshold (LT) and LTV of stMATIC and MATICx on Aave v3 Polygon, on non-eMode.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xcb19a24bca582125febad6d65158d228bc68a2e5f6142446044038f53920a02f](https://etherscan.io/tx/0xcb19a24bca582125febad6d65158d228bc68a2e5f6142446044038f53920a02f)

```
- id: 339
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000ff374ad1be52ff54cf576586253a113d3f48d4b7]
- withDelegatecalls: [true]
- startBlock: 18333141
- endBlock: 18352341
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xe0ac7fa98908e574dbeef273a99959111303e8ee4644f476a12d9087e73bd898
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/339.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/339.md)

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/339_Polygon_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/339_Polygon_pending_0.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://polygonscan.com/address/0xff374ad1be52ff54cf576586253a113d3f48d4b7#code#F1#L15) properly doing the following updates on Aave v3 Polygon, via the Config Engine:

*stMATIC*
- LT: 65% -> **60%**
- LTV: 50% -> **45%**

*MATICx*
- LT: 67% -> **62%**
- LTV: 58% -> **45%**

The proposal is consistent with the discussions on the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
