# Proposal 62. GHO Stewards + Borrow Rate Update.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=62](https://vote.onaave.com/proposal/?proposalId=62)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-gho-stewards-borrow-rate-update/16956](https://governance.aave.com/t/arfc-gho-stewards-borrow-rate-update/16956)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x1a9F90297E3bd848C089cf9D62D7EBB00379Bf77#code#F1#L15)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal sets new interest rate values for gho borrow to match market borrow rates of other established stablecoins.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x51742365a553fd27ff3a669400a426df90dd81db1d1673af84c3889b8de999f6](https://etherscan.io/tx/0x51742365a553fd27ff3a669400a426df90dd81db1d1673af84c3889b8de999f6)

```
- proposalId: 62
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xbe29a6873c3a4a326ac8b4d04132668a0dfc8f25e9b54c48576cbb0a3561019c
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
      "payloadId": "89" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xbe29a6873c3a4a326ac8b4d04132668a0dfc8f25e9b54c48576cbb0a3561019c" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/62.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/62.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/89.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/89.md)

<br>

### Technical analysis

We have verified that the payload changes the GHO interest rate strategy such that the borrow rate is increased to 13.00% APR without changing the max discount rate.


<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
