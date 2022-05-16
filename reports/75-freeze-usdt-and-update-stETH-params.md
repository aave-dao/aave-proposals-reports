# Proposal 75. Freezing UST and Updating stETH Parameters

<br>

### Voting link
[https://app.aave.com/governance/proposal/?proposalId=75](https://app.aave.com/governance/proposal/?proposalId=75)

### Governance forum discussion
[https://governance.aave.com/t/canceling-aip-74-freezing-ust-and-updating-steth-parameters/8154](https://governance.aave.com/t/canceling-aip-74-freezing-ust-and-updating-steth-parameters/8154)

<br>

## BGD analysis

### Proposal types

:wrench: :bar_chart: params-update

:chart_with_downwards_trend: market-driven-update

:ice_cube: freeze-asset

### Context
This proposal freezes UST (given its market instability) and adjust the risk parameters of stETH on Aave v2 Ethereum.

### Proposal creation
Transaction: [https://etherscan.io/tx/0xdff45c73539b96f4a524dbf264779afd81427435e7357562aaa11120b958ef86](https://etherscan.io/tx/0xdff45c73539b96f4a524dbf264779afd81427435e7357562aaa11120b958ef86)
```
- id: 75
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756]
- values: [0,0]
- signatures: [,]
- calldatas: [0x7aca76eb000000000000000000000000a693b19d2931d498c5b318df961919bb4aee87a5,0x7c4e560b000000000000000000000000ae7ab96520de3a18e5e111b5eaab095312d7fe840000000000000000000000000000000000000000000000000000000000001af40000000000000000000000000000000000000000000000000000000000001fa400000000000000000000000000000000000000000000000000000000000029fe]
- withDelegatecalls: [false,false]
- startBlock: 14777131
- endBlock: 14796331
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x1817d9c4e40170c6e2636ac17191c9b51c692fca77813f4378e608256ee9f070
```

### Technical analysis
From a technical perspective, we have verified that the calldata submitted as payload of the proposal does the following:
1. Calls `freezeReserve()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for UST (Wormhole).
2. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for stETH, to set LTV to 69%, Liquidation Threshold to 81%  and Liquidation Bonus to 7.5% (not modified).


### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: Payload encoded via multiple targets and calldatas, no delegatecall

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the payload before the proposal was submitted.

:x: BGD reviewed the procedure followed to submit the proposal.
