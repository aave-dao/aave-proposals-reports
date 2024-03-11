# Proposal 45. Amend Safety Module Emissions.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=45](https://vote.onaave.com/proposal/?proposalId=45)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-amend-safety-module-emissions/16640](https://governance.aave.com/t/arfc-amend-safety-module-emissions/16640)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xaDbe5540140D1b5eB9dcac7Ea20DF95c37287426#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal modifies the daily AAVE emissions across the three Safety Module in order to support GHO stability and the 1:1 peg.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x7b827a57bdad0633b6b3d2ab30960ba936e0e49027a87b3c3b23042f82e7d5c4](https://etherscan.io/tx/0x7b827a57bdad0633b6b3d2ab30960ba936e0e49027a87b3c3b23042f82e7d5c4)

```
- proposalId: 45
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x6079957be200c574924e7da977bc296374ac89604d488a737c19684bf1a2cc45
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "1", 
      "accessLevel": "1", 
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5", 
      "payloadId": "74" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x6079957be200c574924e7da977bc296374ac89604d488a737c19684bf1a2cc45" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/45.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/45.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/74.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/74.md)

<br>

### Technical analysis

We have verified that the payload modifies the daily AAVE emissions of the following Safety Modules:

- stkAAVE:
    Old: 385 AAVE/Day  New: 360 AAVE/Day

- stkBPT:
    Old: 385 AAVE/Day  New: 360 AAVE/Day

- stkGHO:
    Old: 50 AAVE/Day  New: 100 AAVE/Day

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
