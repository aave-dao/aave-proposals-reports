# Proposal 139. Chaos Labs <> Aave engagement extension to cover Aave v2

<br>

### Voting link
[https://app.aave.com/governance/proposal/?proposalId=139](https://app.aave.com/governance/proposal/?proposalId=139)

<br>

### Governance forum discussion
[https://governance.aave.com/t/arc-chaos-labs-aave-v2-coverage/11012](https://governance.aave.com/t/arc-chaos-labs-aave-v2-coverage/11012)

<br>

## BGD analysis

<br>

### Proposal types

:money_with_wings: funds-release

:credit_card: funds-allowance

<br>

### Context
This proposal extends the engagement of Chaos Labs with the Aave DAO to cover Aave v2 instances.

The payload initiates one payment stream of 175'000 aUSDC and another of 1'242 AAVE, pre-calculated to be approximately the 250'000 USD requested.

<br>

### Proposal creation
Transaction: [https://etherscan.io/tx/0x263cf9c0e67fa027d1ff2454a35b6ebe2746263c3fffb1d58e893a9d8655c204](https://etherscan.io/tx/0x263cf9c0e67fa027d1ff2454a35b6ebe2746263c3fffb1d58e893a9d8655c204)

```
- id: 139
- creator: 0xbc540e0729b732fb14afa240aa5a047ae9ba7df0
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x8922235734ec69e956977e2ea9774de8f614053a]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16332530
- endBlock: 16351730
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x331ce7b8a6bd1ee844fa7a041a484b22a36a8d9b4b7d9f598bb5f09cb4377b10
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/139.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/139.md)


<br>

### Technical analysis

We have verified the proposal payload does the following:
1. By interacting with the [AaveEcosystemReserveController](https://etherscan.io/address/0x3d569673dAa0575c936c7c67c4E6AedA69CC630C#code), create a transfer of 175'000 aUSDC from the Aave v2 Ethereum Collector to the address defined as [Chaos recipient](https://etherscan.io/address/0xbC540e0729B732fb14afA240aA5A047aE9ba7dF0).
2. Also by interacting with the [AaveEcosystemReserveController](https://etherscan.io/address/0x3d569673dAa0575c936c7c67c4E6AedA69CC630C#code), create a payment stream of 1'242 AAVE from the AAVE Ecosystem Reserve to the address defined as [Chaos recipient](https://etherscan.io/address/0xbC540e0729B732fb14afA240aA5A047aE9ba7dF0).

The streams duration is 150 days long, considering 30-days months for totalling 5 months, which we consider acceptable.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
