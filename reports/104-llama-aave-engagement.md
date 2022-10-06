# Proposal 104. Llama <> Aave

<br>

### Voting link
[https://app.aave.com/governance/proposal/?proposalId=104](https://app.aave.com/governance/proposal/?proposalId=104)

<br>

### Governance forum discussion
[https://governance.aave.com/t/updated-proposal-llama-aave/9924](https://governance.aave.com/t/updated-proposal-llama-aave/9924)

<br>

## BGD analysis

<br>

### Proposal types

:money_with_wings: funds-release

:credit_card: funds-allowance

<br>

### Context
This proposal bootstraps an engagement for services with Llama with a duration of 12 months, by doing an upfront payment and starting two 12-months streams.

<br>

### Proposal creation
Transaction: [https://etherscan.io/tx/0x225c8d63ddd077b283a944f119d8bf78223cbacf539a7b4cc710450dd54f830e](https://etherscan.io/tx/0x225c8d63ddd077b283a944f119d8bf78223cbacf539a7b4cc710450dd54f830e)

```
- id: 104
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xbdd286d4b9bfbd10319f3fcd1c76e9eca12a80ee]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 15682602
- endBlock: 15701802
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x36aa00386384368237493f0b0d3d309084e1d240ef80198e1d1ea97aa6547c58
```

### Technical analysis
We have verifier the proposal payload does the following:
1. By interacting with the [AaveEcosystemReserveController](https://etherscan.io/address/0x3d569673dAa0575c936c7c67c4E6AedA69CC630C#code), transfers out value of $350'000 aUSDC and $150'000 AAVE to a  Llama's controlled address.
2. Also by interacting with the AaveEcosystemReserveController, creates two payment streams of 12 months, one for value of $700'000 in aUSDC and another for value of $300'000 in AAVE.

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

:white_check_mark: Only one payload used via delegatecall
