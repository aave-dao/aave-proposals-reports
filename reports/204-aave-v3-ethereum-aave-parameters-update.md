# Proposal 204. Aave v3 Ethereum - AAVE parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=204](https://app.aave.com/governance/proposal/?proposalId=204)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-align-aave-risk-parameters-on-aave-v3-ethereum-market-with-aave-v2/12656](https://governance.aave.com/t/arfc-align-aave-risk-parameters-on-aave-v3-ethereum-market-with-aave-v2/12656)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the risk parameters of the AAVE asset on Aave v3 Ethereum, to align them with the ones on Aave v2 Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x359567118d82e370f3f502d2e1fee5fa375bcbb3e5489e5e6380fcff30b2e60c](https://etherscan.io/tx/0x359567118d82e370f3f502d2e1fee5fa375bcbb3e5489e5e6380fcff30b2e60c)

```
- id: 204
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x8afb5a7ec013fe08c36efc9b3b48afed9d53d901]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17074091
- endBlock: 17093291
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x899a2100c271e4cae958d3af62e74717ed2662dbd8ac6ffdc17c4d126ba966ec
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/204.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/204.md)


<br>

### Technical analysis

The [proposal payload](https://etherscan.io/address/0x8afb5a7ec013fe08c36efc9b3b48afed9d53d901#code#F22#L1) effectively does the following changes on the AAVE asset on Aave v3 Ethereum:

- LTV: 60% -> **66%**
- Liquidation Threshold: 70% -> **73%**


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
