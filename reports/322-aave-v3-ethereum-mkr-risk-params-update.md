# Proposal 322. Aave v3 Ethereum - MKR risk parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=322](https://app.aave.com/governance/proposal/?proposalId=322)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-borrowing-cap-expansion-request-mkr/14763](https://governance.aave.com/t/arfc-borrowing-cap-expansion-request-mkr/14763)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the debt ceiling parameter of MKR on Aave v3 Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x03711d4d0e3e144d60db0d9db6b4c84d3124f91872b1850154b6e8c5fe5ce7e7](https://etherscan.io/tx/0x03711d4d0e3e144d60db0d9db6b4c84d3124f91872b1850154b6e8c5fe5ce7e7)

```
- id: 322
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xb2b657c137a7dfd12a0bf082a57fc28aeb49a64d]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 18148047
- endBlock: 18167247
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xfed24b2f6bfc4bc8ca9fd265840761c459af90169a4b00e29776a8afbd989d4c
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/322.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/322.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xb2b657c137a7dfd12a0bf082a57fc28aeb49a64d#code#F1#L13) updates the following parameters on Aave v3 Ethereum, by using the BGD Config Engine:

MKR

- Debt ceiling: 2'500'000 USD -> **6'000'000 USD**

The proposal is consistent with the discussions on the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
