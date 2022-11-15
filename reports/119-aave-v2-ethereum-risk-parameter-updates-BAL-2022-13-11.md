# Proposal 119. Aave v2 Ethereum - Risk Parameter Updates BAL 2022-13-11

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=119](https://app.aave.com/governance/proposal/?proposalId=119)

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

This proposal is an update of risk parameters on Aave v2 Ethereum by Gauntlet, to freeze the BAL asset, motivated by an important situation of volatility in the market.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xdd5266f897c8db86f0120bbd69314391a7c8a38f9130841e96322e023f77bc19](https://etherscan.io/tx/0xdd5266f897c8db86f0120bbd69314391a7c8a38f9130841e96322e023f77bc19)

```
- id: 119
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x311bb771e4f8952e6da169b425e7e92d6ac45756]
- values: [0]
- signatures: []
- calldatas: [0x7aca76eb000000000000000000000000ba100000625a3754423978a60c9317c58a424e3d]
- withDelegatecalls: [false]
- startBlock: 15971584
- endBlock: 15990784
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x61f6e82640afe4b7de943c55426f30eae97d53124e43bb7e28ea39f20ce52359
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/119.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/119.md)

<br>

### Technical analysis

From a technical perspective, we have verified that the calldata submitted as payload of the proposal does the following:

1. Calls `freezeReserve()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for BAL, disabling providing liquidity and borrowing; keeping active repayments and liquidations.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: Payload encoded via multiple targets and calldatas, no delegatecall

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the procedure followed to submit the proposal.
