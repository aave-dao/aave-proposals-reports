# Proposal 92. Aave v2 Ethereum - Risk Parameter Updates 2022/08/03

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=92](https://app.aave.com/governance/proposal/?proposalId=92)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-risk-parameter-updates-for-aave-v2-and-aave-arc-fireblocks-2022-08-04/9197](https://governance.aave.com/t/arc-risk-parameter-updates-for-aave-v2-and-aave-arc-fireblocks-2022-08-04/9197)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal is a periodic update by Gauntlet concerning risk parameters on Aave v2 Ethereum.

It includes lowering of liquidations thresholds which technically could cause liquidation of positions, but following [this Snapshot](https://snapshot.org/#/aave.eth/proposal/bafkreigdmcfmwvnxfolpds4xkdicgrszgmknig7pz2r2t37tltupdpyfu4) approved by the Aave community, the changes are withing the green-lighted limits. In addition, Gauntlet has been diligently updating periodically the community concerning potential liquidations cause by the proposal, and at the time this report is publishing, no liquidation will happen.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x9aa12ef6a1b4917dadf6a6f1839bc3ef02be1814761a61ad49484d1e8edf4d16](https://etherscan.io/tx/0x9aa12ef6a1b4917dadf6a6f1839bc3ef02be1814761a61ad49484d1e8edf4d16)

```
- id: 92
 - creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
 - executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
 - targets: [0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756]
 - values: [0,0,0,0]
 - signatures: [,,,]
 - calldatas: [0x7c4e560b000000000000000000000000d533a949740bb3306d119cc777fa900ba034cd52000000000000000000000000000000000000000000000000000000000000157c00000000000000000000000000000000000000000000000000000000000019000000000000000000000000000000000000000000000000000000000000002a62,0x7c4e560b0000000000000000000000006b175474e89094c44da98b954eedeac495271d0f0000000000000000000000000000000000000000000000000000000000001e14000000000000000000000000000000000000000000000000000000000000213400000000000000000000000000000000000000000000000000000000000028a0,0x7c4e560b000000000000000000000000f629cbd94d3791c9250152bd8dfbdf380e2a3b9c00000000000000000000000000000000000000000000000000000000000017700000000000000000000000000000000000000000000000000000000000001a2c0000000000000000000000000000000000000000000000000000000000002968,0x7c4e560b000000000000000000000000514910771af9ca656af840dff83e8264ecf986ca0000000000000000000000000000000000000000000000000000000000001b58000000000000000000000000000000000000000000000000000000000000206c00000000000000000000000000000000000000000000000000000000000029cc]
 - withDelegatecalls: [false,false,false,false]
 - startBlock: 15310833
 - endBlock: 15330033
 - strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
 - ipfsHash: 0xfc2b36ceb45105fa1c53d81da3c4bd574c576fc13994a68484bab35cb35cd1a1
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/092.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/092.md)

<br>

### Technical analysis

From a technical perspective, we have verified that the calldata submitted as payload of the proposal does the following:

1. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for CRV, to set LTV to 55% (not modified), Liquidation Threshold to 64% (from 65%) and Liquidation Bonus to 8.5% (not modified).
2. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for DAI, to set LTV to 77% (not modified), Liquidation Threshold to 85% (from 80%) and Liquidation Bonus to 4% (from 5%).
3. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for LINK, to set LTV to 70% (not modified), Liquidation Threshold to 83% (from 78%) and Liquidation Bonus to 7% (from 6.3%).
4. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for ENJ, to set LTV to 60% (not modified), Liquidation Threshold to 67% (from 70%) and Liquidation Bonus to 6% (from 6.5%).

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: Payload encoded via multiple targets and calldatas, no delegatecall

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the payload before the proposal was submitted.

:x: BGD reviewed the procedure followed to submit the proposal.
