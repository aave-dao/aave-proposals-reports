# Proposal 65. Borrow Cap Reductions on Aave V3 Ethereum.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=65](https://vote.onaave.com/proposal/?proposalId=65)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-borrow-cap-reductions-on-aave-ethereum-03-11-24/16918](https://governance.aave.com/t/arfc-chaos-labs-borrow-cap-reductions-on-aave-ethereum-03-11-24/16918)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xE9F01095Ae5bc6E3998C730b26554D5C77770258#code#F1#L71)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal aims to reduce the borrow cap of long-tailed asset due to them being a low income source to the protocol, while posing a relatively high risk.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xf50917b0418bf6317d10b8f089af709f1219ca74249a9773dd190fe60220fe57](https://etherscan.io/tx/0xf50917b0418bf6317d10b8f089af709f1219ca74249a9773dd190fe60220fe57)

```
- proposalId: 65
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xbb9f1bab4d67aa7d8f086735042c66e2d7e1ad2126479bc4e4ef1fab676947c5
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
      "payloadId": "91" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xbb9f1bab4d67aa7d8f086735042c66e2d7e1ad2126479bc4e4ef1fab676947c5" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/65.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/65.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/91.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/91.md)

<br>

### Technical analysis

We have verified that the payload sets the following borrow caps to the listed assets without changing the supply caps:

MKR: 1.98k

LDO: 1.5m

UNI: 330k

RPL: 316.8k

SNX: 150k

FXS: 330k

CRV: 2.75m

STG: 3.2m

KNC: 350k

1INCH: 475.2k

BAL: 244.2k

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
