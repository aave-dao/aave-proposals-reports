# Proposal 202. Aave Chan Initiative (ACI) <> Aave engagement

<br>

### Voting link
[https://app.aave.com/governance/proposal/?proposalId=202](https://app.aave.com/governance/proposal/?proposalId=202)

<br>

### Governance forum discussion
[https://governance.aave.com/t/arfc-aci-service-provider-6-month-proposal/12513](https://governance.aave.com/t/arfc-aci-service-provider-6-month-proposal/12513)

<br>

## BGD analysis

<br>

### Proposal types

:credit_card: funds-allowance

<br>

### Context

This proposal bootstraps an engagement for services with ACI (Aave Chan Initiative) for 6 months, in the context of Aave ecosystem's growth and contribution.

The payload initiates one payment stream of 250'000 aUSDT for 180 days.

<br>

### Proposal creation
Transaction: [https://etherscan.io/tx/0xb75fa751c1a81264ac304cfdae2a85d5639980d8317028f65fd9af95fb4f306a](https://etherscan.io/tx/0xb75fa751c1a81264ac304cfdae2a85d5639980d8317028f65fd9af95fb4f306a)

```
- id: 202
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xceb784bc375cdc2a0cd55c06febb9ba32c35f1b1]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17045387
- endBlock: 17064587
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x08e41909ee73087b8cfd0f31a95771ec7321e072e77660c4b9bbc400566b3f68
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/202.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/202.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xceb784bc375cdc2a0cd55c06febb9ba32c35f1b1#code#F5#L25) effectively creates a payment stream of 250'000 aUSDT from the Aave v2/v3 Collector by interacting with the [AaveEcosystemReserveController](https://etherscan.io/address/0x3d569673dAa0575c936c7c67c4E6AedA69CC630C#code), via the `createStream()` function.

The streams duration is effectively 180 days long.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
