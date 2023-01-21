# Proposal 145. Aave Grants DAO Renewal

<br>

### Voting link
[https://app.aave.com/governance/proposal/?proposalId=145](https://app.aave.com/governance/proposal/?proposalId=145)

<br>

### Governance forum discussion
[https://governance.aave.com/t/updated-proposal-aave-grants-dao-renewal/11289/6](https://governance.aave.com/t/updated-proposal-aave-grants-dao-renewal/11289/6)

<br>

## BGD analysis

<br>

### Proposal types

:money_with_wings: funds-release

:credit_card: funds-allowance

<br>

### Context
This proposal gives allowance to Aave Grants DAO to pull approximately 2'437'500 USD (in DAI, aDAI and aUSDT) and ~13'343 AAVE.

<br>

### Proposal creation
Transaction: [https://etherscan.io/tx/0xbc4cc7fb05f3505ab8a24048cecb6a17e9c40447ea87ae5b6930a32c4c1e0d55](https://etherscan.io/tx/0xbc4cc7fb05f3505ab8a24048cecb6a17e9c40447ea87ae5b6930a32c4c1e0d55)

```
- id: 145
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xe4621dfd503a533f42bb5a45162ea3e5233acd5f]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16455480
- endBlock: 16474680
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xf163a78ece7e888b7e2e035557e5307877f08aca09e284a5b8692876e021545a
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/145.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/145.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xe4621dfd503a533f42bb5a45162ea3e5233acd5f#code) does the following:
1. Approves the address defined as [Aave Grants DAO multisig](0x89C51828427F70D77875C6747759fB17Ba10Ceb0) to spend 451'916.32 DAI.
2. Approves the same address to spend 1'172'938.79 DAI.
3. Approves the same address to spend 812'944.90 aUSDT.
4. Approves the same address to spend 13'343.73 AAVE.

Additionally, we have checked that:
- All the interactions are properly doing by calling `approve()` on the [Aave Collector Controller](https://etherscan.io/address/0x3d569673dAa0575c936c7c67c4E6AedA69CC630C#code).
- The Collector and Ecosystem Reserve should have at the moment of execution enough funds to fulfill the allowance.
- The total amount is approximately equivalent to the 3'250'000 USD budgeted.
- The price taken for AAVE is acceptable, being a 30-days average.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
