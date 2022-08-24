# Proposal 94. Aave v2 Ethereum - Risk Parameter Updates 2022/08/18

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=94](https://app.aave.com/governance/proposal/?proposalId=94)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-risk-parameter-updates-for-aave-v2-and-aave-arc-fireblocks-2022-08-18/9367](https://governance.aave.com/t/arc-risk-parameter-updates-for-aave-v2-and-aave-arc-fireblocks-2022-08-18/9367)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal is a periodic update by Gauntlet concerning risk parameters on Aave v2 Ethereum.

It includes lowering of liquidations thresholds which technically could cause liquidation of positions. But Gauntlet has been updating periodically the community concerning potential liquidations cause by the proposal, and at the time this report is publishing, no liquidation will happen.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x9aa12ef6a1b4917dadf6a6f1839bc3ef02be1814761a61ad49484d1e8edf4d16](https://etherscan.io/tx/0x9aa12ef6a1b4917dadf6a6f1839bc3ef02be1814761a61ad49484d1e8edf4d16)

```
- id: 94
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756]
- values: [0,0,0]
- signatures: [,,]
- calldatas: [0x7c4e560b000000000000000000000000d533a949740bb3306d119cc777fa900ba034cd52000000000000000000000000000000000000000000000000000000000000157c00000000000000000000000000000000000000000000000000000000000017d40000000000000000000000000000000000000000000000000000000000002a30,0x7c4e560b0000000000000000000000006b175474e89094c44da98b954eedeac495271d0f0000000000000000000000000000000000000000000000000000000000001e14000000000000000000000000000000000000000000000000000000000000232800000000000000000000000000000000000000000000000000000000000028a0,0x7c4e560b0000000000000000000000002260fac5e5542a773aa44fbcfedf7c193bc2c5990000000000000000000000000000000000000000000000000000000000001b580000000000000000000000000000000000000000000000000000000000001f400000000000000000000000000000000000000000000000000000000000002904]
- withDelegatecalls: [false,false,false]
- startBlock: 15399084
- endBlock: 15418284
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x9c3d2b8a13150c0fc23f277d2f1c0f09e0eb6557ea1e1f0174f5e6ae8d14eeb1
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/094.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/094.md)

<br>

### Technical analysis

From a technical perspective, we have verified that the calldata submitted as payload of the proposal does the following:

1. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for CRV, to set LTV to 55% (not modified), Liquidation Threshold to 61% (from 64%) and Liquidation Bonus to 8% (from 8.5%).
2. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for DAI, to set LTV to 77% (not modified), Liquidation Threshold to 90% (from 85%) and Liquidation Bonus to 4% (not modified).
3. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for WBTC, to set LTV to 70% (not modified), Liquidation Threshold to 80% (from 75%) and Liquidation Bonus to 5% (from 6.5%).

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: Payload encoded via multiple targets and calldatas, no delegatecall

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the payload before the proposal was submitted.

:x: BGD reviewed the procedure followed to submit the proposal.
