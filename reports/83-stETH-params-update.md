# Proposal 83. Freeze stETH, Increase stETH Liq. Threshold to 90%, Pause ETH Borrowing

<br>

### Voting link
[https://app.aave.com/governance/proposal/?proposalId=83](https://app.aave.com/governance/proposal/?proposalId=83)

### Governance forum discussion
[https://governance.aave.com/t/staked-eth-and-aave-risk-june-11th-update/8469](https://governance.aave.com/t/staked-eth-and-aave-risk-june-11th-update/8469)

<br>

## BGD analysis

### Proposal types

:wrench: :bar_chart: params-update

### Context
This proposal targets the change of some risk parameters on stETH, given its market situation.

### Proposal creation
Transaction: [https://etherscan.io/tx/0x5972b3f8a9f3a4d8cf06faca5b65d4bf442c5ff22fe29f6e5455e476e621eb0d](https://etherscan.io/tx/0x5972b3f8a9f3a4d8cf06faca5b65d4bf442c5ff22fe29f6e5455e476e621eb0d)
```
- id: 83
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756]
- values: [0,0,0]
- signatures: [,,]
- calldatas: [0xa8dc0f45000000000000000000000000c02aaa39b223fe8d0a0e5c4f27ead9083c756cc2,0x7aca76eb000000000000000000000000ae7ab96520de3a18e5e111b5eaab095312d7fe84,0x7c4e560b000000000000000000000000ae7ab96520de3a18e5e111b5eaab095312d7fe840000000000000000000000000000000000000000000000000000000000001af4000000000000000000000000000000000000000000000000000000000000232800000000000000000000000000000000000000000000000000000000000029fe]
- withDelegatecalls: [false,false,false]
- startBlock: 14959761
- endBlock: 14978961
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x7cfe8e430467c7c48e4debeb1f8d797eec11c9128f0e23b96857f15335fe7b85
```

### Aave Seatbelt report
[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/083.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/083.md)


### Technical analysis
From a technical perspective, we have verified that the calldata submitted as payload of the proposal does the following:
1. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for stETH, to set LTV to 69% (not modified),  Liquidation Threshold to 90% and Liquidation Bonus to 7.5% (not modified).
2. Calls `freezeReserve()` on [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for stETH, freezing the reserve: only allowing repayments, withdrawals and liquidations, not new borrowings or deposits.
3. Calls `disableBorrowingOnReserve()` on [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for WETH.



### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: Payload encoded via multiple targets and calldatas, no delegatecall

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the payload before the proposal was submitted.

:x: BGD reviewed the procedure followed to submit the proposal.
