# Proposal 135. Treasury Tooling Payment.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=135](https://vote.onaave.com/proposal/?proposalId=135)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-treasury-management-tooling-upgrade/15201](https://governance.aave.com/t/arfc-treasury-management-tooling-upgrade/15201)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x065DF1F9d0aeDEa11E6d059ce29e91d2Abed59fA#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal grants payment to TokenLogic of 12,430 GHO for the delivery of three asset bridging contracts of Optimism, Arbitrum, Plasma.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x6c5b76507fc3e58799b0b0f1efdc8f6ee6e31fd13e3f6f02dc6270ecb367f753](https://etherscan.io/tx/0x6c5b76507fc3e58799b0b0f1efdc8f6ee6e31fd13e3f6f02dc6270ecb367f753)

```
- proposalId: 135
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x3acd9e8619c0ec0c78c5df5aa4d02aaf1ceeef9b3e5946b65e3cc471227a852c
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
      "payloadId": "149" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x3acd9e8619c0ec0c78c5df5aa4d02aaf1ceeef9b3e5946b65e3cc471227a852c" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/135.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/135.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/149.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/149.md)

<br>

### Technical analysis

We have verified that the payload approves 12,430 GHO to TokenLogic's address.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

