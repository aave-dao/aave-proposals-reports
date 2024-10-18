# Proposal 183. USDS Borrow Rate Update.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=183](https://vote.onaave.com/proposal/?proposalId=183)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-increase-usds-borrow-rate-to-match-sky-savings-rate/19494](https://governance.aave.com/t/arfc-increase-usds-borrow-rate-to-match-sky-savings-rate/19494)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x39A47E6fe022529776bD48D47B26fa80aDfce3fb#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal increases the BaseVariableBorrowRate of USDS to 6.25%.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x1d3024225c8ca76d70847b9ded3562cdb707c384ecbe9e396e3b7a03fa864a61](https://etherscan.io/tx/0x1d3024225c8ca76d70847b9ded3562cdb707c384ecbe9e396e3b7a03fa864a61)

```
- proposalId: 183
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x8ece2cc5d2a006f83bc7d5a1cc8b889842390f7bb96b40963e68d1143a5d27d6
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
      "payloadId": "192" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x8ece2cc5d2a006f83bc7d5a1cc8b889842390f7bb96b40963e68d1143a5d27d6" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/183.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/183.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/196.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/196.md)

<br>

### Technical analysis

We have verified that the payloads increases the borrow rate of USDS to 6.25%.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
