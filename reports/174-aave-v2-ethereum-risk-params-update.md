# Proposal 174. Aave v2 Ethereum - MKR risk params update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=174](https://app.aave.com/governance/proposal/?proposalId=174)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-chaos-labs-risk-parameter-updates-mkr-on-aave-v2-ethereum-2023-02-17/11948](https://governance.aave.com/t/arc-chaos-labs-risk-parameter-updates-mkr-on-aave-v2-ethereum-2023-02-17/11948)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the risk parameters of MKR on Aave v2 Ethereum.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xc5d7b9b224bb56757a5b66eb22d076bdee3ca79c17a9b9deb390921eddeccee5](https://etherscan.io/tx/0xc5d7b9b224bb56757a5b66eb22d076bdee3ca79c17a9b9deb390921eddeccee5)

```
- id: 174
- creator: 0xbc540e0729b732fb14afa240aa5a047ae9ba7df0
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x014b2fc091cad41f5d6a8eeb2fef27852f4a97e7]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16784927
- endBlock: 16804127
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xcce5f7fcad7db1ff6ac26c62dcb85cca41186d8a8eb3e770689ac0aba267d60f
```

<br>

### Aave Seatbelt reports

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/174.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/174.md)


<br>

### Technical analysis

From a technical perspective, we have verified the [proposal payload](https://etherscan.io/address/0x014b2fc091cad41f5d6a8eeb2fef27852f4a97e7#code#F3#L14) changes the following risk parameters by interacting with the [PoolConfigurator of Aave v2 Ethereum](https://etherscan.io/address/0x311Bb771e4F8952E6Da169b425E7e92d6Ac45756):

- MKR:
  - LTV: 62% -> **59%**
  - Liquidation Threshold: 67% -> **74%**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
