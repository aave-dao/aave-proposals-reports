# Proposal 117. Aave v2 Ethereum - Risk Parameter Updates REN 2022-12-11

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=117](https://app.aave.com/governance/proposal/?proposalId=117)

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

This proposal is an update of risk parameters on Aave v2 Ethereum by Gauntlet, to freeze the REN asset, motivated by an important situation of volatility in the market.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xb388da860f6d2ec2a27ba29147ce7285ed8102f9a4783d6d3f8d6e44a908b561](https://etherscan.io/tx/0xb388da860f6d2ec2a27ba29147ce7285ed8102f9a4783d6d3f8d6e44a908b561)

```
- id: 117
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x311bb771e4f8952e6da169b425e7e92d6ac45756]
- values: [0]
- signatures: []
- calldatas: [0x7aca76eb000000000000000000000000408e41876cccdc0f92210600ef50372656052a38]
- withDelegatecalls: [false]
- startBlock: 15965387
- endBlock: 15984587
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x1a19a9cdef0a9717596c08cec5ecf4786dbe044668d3d139cc8a32931bea8012
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/117.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/117.md)

<br>

### Technical analysis

From a technical perspective, we have verified that the calldata submitted as payload of the proposal does the following:

1. Calls `freezeReserve()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for REN, disabling providing liquidity and borrowing; keeping active repayments and liquidations.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: Payload encoded via multiple targets and calldatas, no delegatecall

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the procedure followed to submit the proposal.
