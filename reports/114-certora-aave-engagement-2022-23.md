# Proposal 114. Certora <> Aave engagement for 2022/2023

<br>

### Voting link
[https://app.aave.com/governance/proposal/?proposalId=114](https://app.aave.com/governance/proposal/?proposalId=114)

<br>

### Governance forum discussion
[https://governance.aave.com/t/security-and-agility-of-aave-smart-contracts-via-continuous-formal-verification/10181](https://governance.aave.com/t/security-and-agility-of-aave-smart-contracts-via-continuous-formal-verification/10181)

<br>

## BGD analysis

<br>

### Proposal types

:money_with_wings: funds-release

:credit_card: funds-allowance

<br>

### Context
This proposal bootstraps an engagement for services with Certora for 1 year, in the context of security assessment and formal verification.
The payload initiates one payment stream of 1'890'000 aUSDC, and another of 9'957 AAVE.

<br>

### Proposal creation
Transaction: [https://etherscan.io/tx/0x7a8e6121dfd595c21bc154dbcb44c4032637bbebdfcdf6cf3653d610f3f19485](https://etherscan.io/tx/0x7a8e6121dfd595c21bc154dbcb44c4032637bbebdfcdf6cf3653d610f3f19485)

```
- id: 114
- creator: 0x070341aa5ed571f0fb2c4a5641409b1a46b4961b
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x2d2b1bf70d98ae9a8cc9a3d7a49c2d321ecc6c04]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 15933758
- endBlock: 15952958
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x8c5c6b73375a981af5e6b8b1cf860500f5c2cfc0570a98203b7f6b48c03d42ba
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/114.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/114.md)


<br>

### Technical analysis
We have verified the proposal payload does the following:
1. By interacting with the [AaveEcosystemReserveController](https://etherscan.io/address/0x3d569673dAa0575c936c7c67c4E6AedA69CC630C#code), create a payment stream of aUSDC from the Aave v2 Ethereum Collector to the address defined as [Certora beneficiary](https://etherscan.io/address/0x0F11640BF66e2D9352d9c41434A5C6E597c5e4c8).
1. Also by interacting with the [AaveEcosystemReserveController](https://etherscan.io/address/0x3d569673dAa0575c936c7c67c4E6AedA69CC630C#code), create a payment stream of AAVE from the AAVE Ecosystem Reserve to the address defined as [Certora beneficiary](https://etherscan.io/address/0x0F11640BF66e2D9352d9c41434A5C6E597c5e4c8).

The stream duration is 360 days long, considering 30-days months for totalling 1 year, which we consider acceptable.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
