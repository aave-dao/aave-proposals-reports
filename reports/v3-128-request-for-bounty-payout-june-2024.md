# Proposal 128. Request for Bounty Payout - June 2024.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=128](https://vote.onaave.com/proposal/?proposalId=128)

<br>

### Governance forum discussion

[https://governance.aave.com/t/bgd-request-for-bounty-payout-june-2024/18119](https://governance.aave.com/t/bgd-request-for-bounty-payout-june-2024/18119)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x69417fd4aeC1B14DEB633B0D210aD53428b323B7#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal will release a total of 1,100 GHO, 1,000 as bounty for one Aave-Immunefi valid submission, and 100 as fee to the Immunefi platform

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x9c6d69b902aeae760ae0529bfb38c7815d7f3b6baa0be6746fc82e3b09583f90](https://etherscan.io/tx/0x9c6d69b902aeae760ae0529bfb38c7815d7f3b6baa0be6746fc82e3b09583f90)

```
- proposalId: 128
- creator: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- accessLevel: 1
- ipfsHash: 0xbc7f448d432e8e43bca5e0738c59aeb796c1f7e7e3c000ad46e39b9e77ccac92
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
      "payloadId": "143"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0xbc7f448d432e8e43bca5e0738c59aeb796c1f7e7e3c000ad46e39b9e77ccac92"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/128.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/128.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/143.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/143.md)

<br>

### Technical analysis

We have verified that the payloads transfers 1,000 GHO to the address provided by the white-hat and 100 GHO to the Immunefi address as fee payment.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

