# Proposal 40. GHO Borrow Rate Increase 2024-02-29

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=40](https://vote.onaave.com/proposal/?proposalId=40)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-increase-gho-borrow-rate-29-02-2024/16787](https://governance.aave.com/t/arfc-increase-gho-borrow-rate-29-02-2024/16787)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x782f46853885d3E3482Ec2cFffaB86F7c9097138#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal increases the gho borrowing rate on the protocol to align with the market rates in order to support the current gho pegging.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xe4e6f67d2da27c9b08a135f4c24d86a442a8a40a70419fc98aecaa2b781b8ccc](https://etherscan.io/tx/0xe4e6f67d2da27c9b08a135f4c24d86a442a8a40a70419fc98aecaa2b781b8ccc)

```
- proposalId: 40
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xb0cb4e66131b2fde2206963b7e70e49d2366e41b54133861f0552538b1804b9c
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
      "payloadId": "70" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xb0cb4e66131b2fde2206963b7e70e49d2366e41b54133861f0552538b1804b9c" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/40.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/40.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/70.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/70.md)

<br>

### Technical analysis

We have verified that the payload changes the GHO interest rate strategy such that the borrow rate is increased to 7.22% without changing the max discount rate.

<br>

The proposal is consistent with the description on the governance forum. It also follows an accelerated procedure following the approval of AIP-381 which pre-approved ACI to perform changes in GHO borrow rate up to 1% with some limitations. [see AIP here](https://governance-v2.aave.com/governance/proposal/381/).

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
