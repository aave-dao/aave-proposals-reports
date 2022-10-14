# Proposal 108. Aave v2 Ethereum - Risk Parameter Updates 2022/10/06

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=108](https://app.aave.com/governance/proposal/?proposalId=108)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-risk-parameter-updates-for-aave-v2-and-aave-arc-fireblocks-2022-10-06/10201](https://governance.aave.com/t/arc-risk-parameter-updates-for-aave-v2-and-aave-arc-fireblocks-2022-10-06/10201)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal is a periodic update by Gauntlet concerning risk parameters on Aave v2 Ethereum.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x892dd57cb84cb4bf849ea23ecf04b180337446921f6e7f01ead94324a3193472](https://etherscan.io/tx/0x892dd57cb84cb4bf849ea23ecf04b180337446921f6e7f01ead94324a3193472)

```
- id: 108
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756]
- values: [0,0]
- signatures: [,]
- calldatas: [0x7c4e560b000000000000000000000000ae7ab96520de3a18e5e111b5eaab095312d7fe840000000000000000000000000000000000000000000000000000000000001c20000000000000000000000000000000000000000000000000000000000000206c00000000000000000000000000000000000000000000000000000000000029cc,0x7c4e560b0000000000000000000000002260fac5e5542a773aa44fbcfedf7c193bc2c5990000000000000000000000000000000000000000000000000000000000001c2000000000000000000000000000000000000000000000000000000000000020080000000000000000000000000000000000000000000000000000000000002904]
- withDelegatecalls: [false,false]
- startBlock: 15729255
- endBlock: 15748455
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x395aff2bbd4c0f988d0aff6de287ddff2c1c5eb847795c9f31618b2261fc34a0
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/108.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/108.md)

<br>

### Technical analysis

From a technical perspective, we have verified that the calldata submitted as payload of the proposal does the following:

1. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for stETH, with the following changes:
    - LTV: **69% -> 72%**
    - Liquidation Threshold: **81% -> 83%**
    - Liquidation Bonus: **7.5% -> 7%**
2. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for WBTC, with the following changes:
    - LTV: **70% -> 72%**
    - Liquidation Threshold: **80% -> 82%**
    - Liquidation Bonus: 5% -> 5%

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: Payload encoded via multiple targets and calldatas, no delegatecall

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the procedure followed to submit the proposal.
