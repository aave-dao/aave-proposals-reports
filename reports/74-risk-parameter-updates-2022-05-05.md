# Proposal 74. Risk Parameter Updates 2022/05/05

<br>

### Voting link
[https://app.aave.com/governance/proposal/?proposalId=74](https://app.aave.com/governance/proposal/?proposalId=74)

### Governance forum discussion
[https://governance.aave.com/t/arc-risk-parameter-updates-2022-05-05/8068](https://governance.aave.com/t/arc-risk-parameter-updates-2022-05-05/8068)

<br>

## BGD analysis

### Proposal types

:wrench: :bar_chart: params-update

:repeat: periodic-proposal

### Context
This proposal is a periodic update by Gauntlet concerning risk parameters on Aave v2 Ethereum. 

### Proposal creation
Transaction: [https://etherscan.io/tx/0xcd6ff521142d523348d13662a56dfe2c1b6cb68750c731112085ba084043754d](https://etherscan.io/tx/0xcd6ff521142d523348d13662a56dfe2c1b6cb68750c731112085ba084043754d)
```
- id: 74
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756]
- values: [0,0,0,0,0]
- signatures: [,,,,]
- calldatas: [0x7c4e560b000000000000000000000000ba100000625a3754423978a60c9317c58a424e3d00000000000000000000000000000000000000000000000000000000000018380000000000000000000000000000000000000000000000000000000000001b5800000000000000000000000000000000000000000000000000000000000029cc,0x7c4e560b0000000000000000000000006b175474e89094c44da98b954eedeac495271d0f0000000000000000000000000000000000000000000000000000000000001e1400000000000000000000000000000000000000000000000000000000000021340000000000000000000000000000000000000000000000000000000000002904,0x7c4e560b000000000000000000000000ae7ab96520de3a18e5e111b5eaab095312d7fe840000000000000000000000000000000000000000000000000000000000001db00000000000000000000000000000000000000000000000000000000000001e1400000000000000000000000000000000000000000000000000000000000029fe,0x7c4e560b0000000000000000000000008798249c2e607446efb7ad49ec89dd1865ff4272000000000000000000000000000000000000000000000000000000000000125c00000000000000000000000000000000000000000000000000000000000019640000000000000000000000000000000000000000000000000000000000002a30,0x7c4e560b0000000000000000000000000bc529c00c6401aef6d220be8c6ea1667f6ad93e00000000000000000000000000000000000000000000000000000000000011f80000000000000000000000000000000000000000000000000000000000001a9000000000000000000000000000000000000000000000000000000000000029fe]
- withDelegatecalls: [false,false,false,false,false]
- startBlock: 14751483
- endBlock: 14770683
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x9b69bc6b214f9510817259012e222af073bc49c8077a2ffe5e6a106508f80b3b
```

### Technical analysis
From a technical perspective, we have verified that the calldata submitted as payload of the proposal does the following:
1. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for BAL, to set LTV to 62%, Liquidation Threshold to 70% (not modified) and Liquidation Bonus to 7%.
2. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for DAI, to set LTV to 77% (not modified), Liquidation Threshold to 85%  and Liquidation Bonus to 5% (not modified).
3. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for stETH, to set LTV to 76%, Liquidation Threshold to 77% and Liquidation Bonus to 7.5% (not modified).
4. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for xSUSHI, to set LTV to 47%, Liquidation Threshold to 65% (not modified) and Liquidation Bonus to 8%.
5. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for YFI, to set LTV to 46%, Liquidation Threshold to 68% and Liquidation Bonus to 7.5% (not modified).


### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: Payload encoded via multiple targets and calldatas, no delegatecall

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the payload before the proposal was submitted.

:x: BGD reviewed the procedure followed to submit the proposal.
