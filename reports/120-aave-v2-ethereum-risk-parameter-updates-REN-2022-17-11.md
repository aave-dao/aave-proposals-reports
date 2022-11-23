# Proposal 120. Aave v2 Ethereum - Risk Parameter Updates REN 2022-17-11

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=120](https://app.aave.com/governance/proposal/?proposalId=120)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-risk-parameter-updates-for-aave-v2-eth-and-aave-arc-fireblocks-2022-11-17/10688](https://governance.aave.com/t/arc-risk-parameter-updates-for-aave-v2-eth-and-aave-arc-fireblocks-2022-11-17/10688)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal is an update of risk parameters on Aave v2 Ethereum by Gauntlet, to reduce REN risk parameters, following the previous freezing on [proposal 117](https://app.aave.com/governance/proposal/?proposalId=117).


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xbabb13c0e95905dd56fbfe1317ca5778dd9259af6c40f60588e3f06a52983e0f](https://etherscan.io/tx/0xbabb13c0e95905dd56fbfe1317ca5778dd9259af6c40f60588e3f06a52983e0f)

```
- id: 120
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x311bb771e4f8952e6da169b425e7e92d6ac45756]
- values: [0]
- signatures: []
- calldatas: [0x7c4e560b000000000000000000000000408e41876cccdc0f92210600ef50372656052a38000000000000000000000000000000000000000000000000000000000000157c000000000000000000000000000000000000000000000000000000000000177000000000000000000000000000000000000000000000000000000000000029fe]
- withDelegatecalls: [false]
- startBlock: 16030143
- endBlock: 16049343
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x693959e01abc68712755e9e55809db89991b3762970eb8a97d84d01e17569ec5
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/120.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/120.md)

<br>

### Technical analysis

From a technical perspective, we have verified that the calldata submitted as payload of the proposal does the following:

1. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for REN, with the following changes:
    - LTV: **60% -> 55%**
    - Liquidation Threshold: **65% -> 60%**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: Payload encoded via multiple targets and calldatas, no delegatecall

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the procedure followed to submit the proposal.
