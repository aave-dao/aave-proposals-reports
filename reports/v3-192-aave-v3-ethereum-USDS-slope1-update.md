# Proposal 192. USDS Slope1 Update.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=192](https://vote.onaave.com/proposal/?proposalId=192)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-increase-usds-borrow-rate-to-match-sky-savings-rate/19494](https://governance.aave.com/t/arfc-increase-usds-borrow-rate-to-match-sky-savings-rate/19494)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x3EA03216c8C186cF6D874F4594E66Fe0F3048F54#code)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal adjusts the variable slope1 of USDS on the Ethereum Mainet market to 0.75% in order to match Sky Savings rate.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x1d74a424a0ad8ec3bf592b1de6df8d87ec7e292decabf89d71ffb49b7e1bfc6b](https://etherscan.io/tx/0x1d74a424a0ad8ec3bf592b1de6df8d87ec7e292decabf89d71ffb49b7e1bfc6b)

```
- proposalId: 192
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x3fda4736d4b519e9b9a6ef75799e21b68028c8f663914bc64b5fad98730a0b8c
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
      "payloadId": "199" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x3fda4736d4b519e9b9a6ef75799e21b68028c8f663914bc64b5fad98730a0b8c" 
}

```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/192.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/192.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/199.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/199.md)

<br>

### Technical analysis

We have verified that the payload modifies slope1 of USDS on the Ethereum Maaine market:

- variable slope1: From: 6.5%  To: 0.75%.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

