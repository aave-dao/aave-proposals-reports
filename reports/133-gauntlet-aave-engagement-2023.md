# Proposal 133. Gauntlet <> Aave engagement for 2023

<br>

### Voting link
[https://app.aave.com/governance/proposal/?proposalId=133](https://app.aave.com/governance/proposal/?proposalId=133)

<br>

### Governance forum discussion
[https://governance.aave.com/t/arc-updated-gauntlet-aave-renewal/11013](https://governance.aave.com/t/arc-updated-gauntlet-aave-renewal/11013)

<br>

## BGD analysis

<br>

### Proposal types

:money_with_wings: funds-release

:credit_card: funds-allowance

<br>

### Context
This proposal bootstraps an engagement for services with Gauntlet for 1 year, in the context of risk parameters recommendations.

The payload initiates one payment stream of 800'000 aUSDC, another of 9'919 AAVE and an upfront payment of 600'000 aUSDC.

<br>

### Proposal creation
Transaction: [https://etherscan.io/tx/0x78c8b4abfccd93611db9de76e337a18cb222b4f3c1306816b8013198ad1c5bc1](https://etherscan.io/tx/0x78c8b4abfccd93611db9de76e337a18cb222b4f3c1306816b8013198ad1c5bc1)

```
- id: 133
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x03232b5ee80369a88620615f8328beec1884b731]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16229094
- endBlock: 16248294
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x98f5bcf905c773dbb9d5336b52f8f6aea62254c092de928fd45b1a4cef5129a7
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/133.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/133.md)


<br>

### Technical analysis

We have verified the proposal payload does the following:
1. By interacting with the [AaveEcosystemReserveController](https://etherscan.io/address/0x3d569673dAa0575c936c7c67c4E6AedA69CC630C#code), create a transfer of 600'000 aUSDC from the Aave v2 Ethereum Collector to the address defined as [Gauntlet beneficiary](https://etherscan.io/address/0xD20c9667bf0047F313228F9fE11F8b9F8Dc29bBa).
2. By interacting with the [AaveEcosystemReserveController](https://etherscan.io/address/0x3d569673dAa0575c936c7c67c4E6AedA69CC630C#code), create a payment stream of 800'000 aUSDC from the Aave v2 Ethereum Collector to the address defined as [Gauntlet beneficiary](https://etherscan.io/address/0xD20c9667bf0047F313228F9fE11F8b9F8Dc29bBa).
1. Also by interacting with the [AaveEcosystemReserveController](https://etherscan.io/address/0x3d569673dAa0575c936c7c67c4E6AedA69CC630C#code), create a payment stream of 9'919 AAVE from the AAVE Ecosystem Reserve to the address defined as [Gauntlet beneficiary](https://etherscan.io/address/0xD20c9667bf0047F313228F9fE11F8b9F8Dc29bBa).

The streams duration is 360 days long, considering 30-days months for totalling 1 year, which we consider acceptable.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
