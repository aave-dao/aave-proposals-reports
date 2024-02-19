# Proposal 28. Chaos Labs Risk Parameter Updates - Increase Debt Ceiling for SNX and MKR on V3 Ethereum - 01.31.2024.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=28](https://vote.onaave.com/proposal/?proposalId=28)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-increase-debt-ceiling-for-snx-and-mkr-on-v3-ethereum-01-31-2024/16480/1](https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-increase-debt-ceiling-for-snx-and-mkr-on-v3-ethereum-01-31-2024/16480/1)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x172c63Ea1c7A92cd06a6362f2190605f71f30D96#code#F29#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal increases the debt ceiling of the following assets on Aave-V3-Ethereum: SNX, MKR since both tokens has reached high utilization - 94%, 99% respectively.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x8d8e160969a6443725d2ce7c39a9c5f05552afd78e43c1874a67b00a0611273c](https://etherscan.io/tx/0x8d8e160969a6443725d2ce7c39a9c5f05552afd78e43c1874a67b00a0611273c)

```
- proposalId: 28
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x6a98f5da75561ecd119ee401e6c7956b71d709ad0892461aef49692aa06fafc5
```

<br>

**createProposal() parameters**

```
{
  "payloads": [
    {
      "chain": "1",
      "accessLevel": 1,
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
      "payloadId": "63"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0x6a98f5da75561ecd119ee401e6c7956b71d709ad0892461aef49692aa06fafc5"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/28.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/28.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/63.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/63.md)

<br>

### Technical analysis

We have verified that the payload modifies the debt ceiling of the following tokens:

SNX: From: 2.5M To: 4M

MKR: From: 8.5M To: 12M

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
