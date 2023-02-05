# Proposal 148. Aave v2 Ethereum - update TUSD and USDT interest rate strategies

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=148](https://app.aave.com/governance/proposal/?proposalId=148)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-interest-rate-curve-changes-for-aave-v2-eth-november-2022/10884](https://governance.aave.com/t/arc-interest-rate-curve-changes-for-aave-v2-eth-november-2022/10884)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the interest rate strategy for TUSD and USDT on the Aave v2 Ethereum pool, together with the Reserve Factor of TUSD.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x105816995d2dae16b3d032b5ee4ecba214f96d3dc90790cd38c1ce0181414ab0](https://etherscan.io/tx/0x105816995d2dae16b3d032b5ee4ecba214f96d3dc90790cd38c1ce0181414ab0)

```
- id: 148
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756]
- values: [0,0,0]
- signatures: [,,]
- calldatas: [0x4b4e67530000000000000000000000000000000000085d4780b73119b644ae5ecd22b37600000000000000000000000000000000000000000000000000000000000001f4,0x1d2118f9000000000000000000000000dac17f958d2ee523a2206206994597c13d831ec700000000000000000000000033deac0861fd6a9235b86172aa939e79085c6f52,0x1d2118f90000000000000000000000000000000000085d4780b73119b644ae5ecd22b3760000000000000000000000006bce15b789e537f3aba3c60cb183f0e8737f05ec]
- withDelegatecalls: [false,false,false]
- startBlock: 16530723
- endBlock: 16549923
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xbab0c676efd10ba3ba04e8f66c69fbb8a0cf3b2ad100348e920b9257d47b1af0
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/148.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/148.md)

**There seems to be some infrastructure problem on Tenderly, which causes the state transitions to show erroneously (`aTokenAddress` instead of the correct `interestRateStrategyAddress`). We have double checked both payload code and events emitted, and everything seems correct**

<br>

### Technical analysis

The proposal payloads do the following:
- Call the [Pool Configurator of Aave v2 Ethereum](https://etherscan.io/address/0x311Bb771e4F8952E6Da169b425E7e92d6Ac45756) to set the Reserve Factor of TUSD to 5%.
- Call the [Pool Configurator of Aave v2 Ethereum](https://etherscan.io/address/0x311Bb771e4F8952E6Da169b425E7e92d6Ac45756) to replace the current interest rate strategy of TUSD with the one on deployed [HERE](https://etherscan.io/address/0x6bcE15B789e537f3abA3C60CB183F0E8737f05eC#code). We verified that the only changes are on slope 2 of variable and rate, passing from 75% to 100%.
- Call the [Pool Configurator of Aave v2 Ethereum](https://etherscan.io/address/0x311Bb771e4F8952E6Da169b425E7e92d6Ac45756) to replace the current interest rate strategy of USDT with the one on deployed [HERE](https://etherscan.io/address/0x33DeAc0861FD6a9235b86172AA939E79085c6f52#code). We verified that the only changes are on slope 2 of variable and rate, passing from 60% to 75%, together with moving the optimal utilization from 90% to 80%.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: Payload encoded via multiple targets and calldatas, no delegatecall

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the procedure followed to submit the proposal.
