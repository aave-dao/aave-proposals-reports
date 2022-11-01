# Proposal 113. Chaos Labs <> Aave

<br>

### Voting link
[https://app.aave.com/governance/proposal/?proposalId=113](https://app.aave.com/governance/proposal/?proposalId=113)

<br>

### Governance forum discussion
[https://governance.aave.com/t/updated-proposal-chaos-labs-risk-simulation-platform/10025](https://governance.aave.com/t/updated-proposal-chaos-labs-risk-simulation-platform/10025)

<br>

## BGD analysis

<br>

### Proposal types

:money_with_wings: funds-release

:credit_card: funds-allowance

<br>

### Context
This proposal bootstraps an engagement for services with Chaos Labs, in the context of risk assessment, parameters recommendation and tooling.
The payload initiates a payment stream of 500'000 aUSDC, starting 6 months after proposal execution, and ending 6 months later.

<br>

### Proposal creation
Transaction: [https://etherscan.io/tx/0xa49bf1ae3f359f5b452d356bd113e2522edd9c733731c0756c29abb1675fe77e](https://etherscan.io/tx/0xa49bf1ae3f359f5b452d356bd113e2522edd9c733731c0756c29abb1675fe77e)

```
- id: 113
- creator: 0xbc540e0729b732fb14afa240aa5a047ae9ba7df0
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x691b41805f7ef2d7de6165bc42295b035a31600d]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 15876593
- endBlock: 15895793
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x5d0543d0e66abc240eceeae5ada6240d4d6402c2ccfe5ad521824dc36be71c45
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/113.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/113.md)


<br>

### Technical analysis
We have verified the proposal payload does the following:
1. By interacting with the [AaveEcosystemReserveController](https://etherscan.io/address/0x3d569673dAa0575c936c7c67c4E6AedA69CC630C#code), create a payment stream of aUSDC from the Aave v2 Ethereum Collector to the address defined as [Chaos Labs recipient wallet](https://etherscan.io/address/0xbC540e0729B732fb14afA240aA5A047aE9ba7dF0).

The stream is defined considering 30-days months, which we consider acceptable.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:x: BGD reviewed the procedure followed to submit the proposal.
