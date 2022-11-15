# Proposal 118. Aave v2 Ethereum - Risk Parameter Updates CVX 2022-13-11

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=118](https://app.aave.com/governance/proposal/?proposalId=118)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-market-downturn-gauntlet-analysis-november-2022/10625](https://governance.aave.com/t/arc-market-downturn-gauntlet-analysis-november-2022/10625)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal is an update of risk parameters on Aave v2 Ethereum by Gauntlet, to freeze the CVX asset, motivated by an important situation of volatility in the market.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xc77b88af4f846fc52c9b1f3ac67be2c96b529376383dc5d5b8530e0a5e44e6c5](https://etherscan.io/tx/0xc77b88af4f846fc52c9b1f3ac67be2c96b529376383dc5d5b8530e0a5e44e6c5)

```
- id: 118
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x311bb771e4f8952e6da169b425e7e92d6ac45756]
- values: [0]
- signatures: []
- calldatas: [0x7aca76eb0000000000000000000000004e3fbd56cd56c3e72c1403e103b45db9da5b9d2b]
- withDelegatecalls: [false]
- startBlock: 15971570
- endBlock: 15990770
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xfd4ed52d0e0728752f11ab23c3b3404009e46562a691520620f46e64ffdf05b4
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/118.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/118.md)

<br>

### Technical analysis

From a technical perspective, we have verified that the calldata submitted as payload of the proposal does the following:

1. Calls `freezeReserve()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for CVX, disabling providing liquidity and borrowing; keeping active repayments and liquidations.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: Payload encoded via multiple targets and calldatas, no delegatecall

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the procedure followed to submit the proposal.
