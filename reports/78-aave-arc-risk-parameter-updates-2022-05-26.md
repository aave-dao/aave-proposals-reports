# Proposal 78. Aave V2 and Arc - Risk Parameter Updates 2022/05/26

<br>

### Voting link
[https://app.aave.com/governance/proposal/?proposalId=78](https://app.aave.com/governance/proposal/?proposalId=78)

### Governance forum discussion
[https://governance.aave.com/t/arc-risk-parameter-updates-for-aave-v2-and-aave-arc-fireblocks-2022-05-26/8299](https://governance.aave.com/t/arc-risk-parameter-updates-for-aave-v2-and-aave-arc-fireblocks-2022-05-26/8299)

<br>

## BGD analysis

### Proposal types

:wrench: :bar_chart: params-update

:repeat: periodic-proposal

:shinto_shrine: Aave Arc

### Context
This proposal is a periodic update by Gauntlet concerning risk parameters on Aave v2 Ethereum, together with another update of parameters but on Aave Arc. Concerning Arc, this proposal only queues the parameters update on the Arc timelock.

### Proposal creation
Transaction: [https://etherscan.io/tx/0x6bb93fdb3330c8aae8d5c5b83f89082d4ed60f3bf4b905b51d8043e3b0e07b96](https://etherscan.io/tx/0x6bb93fdb3330c8aae8d5c5b83f89082d4ed60f3bf4b905b51d8043e3b0e07b96)
```
- id: 78
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0xace1d11d836cb3f51ef658fd4d353ffb3c301218]
- values: [0,0,0,0]
- signatures: [,,,]
- calldatas: [0x7c4e560b000000000000000000000000514910771af9ca656af840dff83e8264ecf986ca0000000000000000000000000000000000000000000000000000000000001a2c0000000000000000000000000000000000000000000000000000000000001d4c0000000000000000000000000000000000000000000000000000000000002904,0x7c4e560b0000000000000000000000002260fac5e5542a773aa44fbcfedf7c193bc2c5990000000000000000000000000000000000000000000000000000000000001af40000000000000000000000000000000000000000000000000000000000001db00000000000000000000000000000000000000000000000000000000000002904,0x7c4e560b000000000000000000000000c02aaa39b223fe8d0a0e5c4f27ead9083c756cc20000000000000000000000000000000000000000000000000000000000001fa4000000000000000000000000000000000000000000000000000000000000206c00000000000000000000000000000000000000000000000000000000000028a0,0xd9a4cbdf00000000000000000000000000000000000000000000000000000000000000a000000000000000000000000000000000000000000000000000000000000000e000000000000000000000000000000000000000000000000000000000000001200000000000000000000000000000000000000000000000000000000000000180000000000000000000000000000000000000000000000000000000000000028000000000000000000000000000000000000000000000000000000000000000010000000000000000000000004e1c7865e7be78a7748724fa0409e88dc14e67aa000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000847c4e560b000000000000000000000000a0b86991c6218b36c1d19d4a2e9eb0ce3606eb48000000000000000000000000000000000000000000000000000000000000222e000000000000000000000000000000000000000000000000000000000000232800000000000000000000000000000000000000000000000000000000000028d20000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000]
- withDelegatecalls: [false,false,false,false]
- startBlock: 14881782
- endBlock: 14900982
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x29d4dbad632008b34cad12727998bb949d898e4d4574d46d3b44701ac21f3b13
```

### Aave Seatbelt report
[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/078.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/078.md)

### Technical analysis
From a technical perspective, we have verified that the calldata submitted as payload of the proposal does the following on Aave V2 Ethereum:
1. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for LINK, to set LTV to 67%, Liquidation Threshold to 75% and Liquidation Bonus to 5%.
2. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for WETH, to set LTV to 81%, Liquidation Threshold to 83%  and Liquidation Bonus to 4%.
3. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for WBTC, to set LTV to 69%, Liquidation Threshold to 76% and Liquidation Bonus to 5%.

**IMPORTANT!!!** This proposal lowers the Liquidation Threshold for active positions using WETH and LINK as collateral, potentially placing them in liquidation if prior to proposal's execution, their HF is too close to 1.

On the Aave Arc side, this proposal proposal queues on the Aave Arc timelock a payload that, if approved, will do the following changes:
1. Calls `configureReserveAsCollateral()` on the [Arc Aave Pool Configurator](https://etherscan.io/address/0x4e1c7865e7be78a7748724fa0409e88dc14e67aa#code) for USDC, to set LTV to 87.5%, Liquidation Threshold to 90% and Liquidation Bonus to 4.5% (not modified).


### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: Payload encoded via multiple targets and calldatas, no delegatecall

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the payload before the proposal was submitted.

:x: BGD reviewed the procedure followed to submit the proposal.

:x: Potential unintended side effects properly disclosed pre-proposal.
