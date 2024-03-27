# Proposal 58. Remove ARB from Isolation Mode on Arbitrum.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=58](https://vote.onaave.com/proposal/?proposalId=58)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-remove-arb-from-isolation-mode-on-arbitrum-market/16703](https://governance.aave.com/t/arfc-remove-arb-from-isolation-mode-on-arbitrum-market/16703)

<br>

### Payloads

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x9f6fFf167A24A9E4245b025e1185d8601F6b431f#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal suggests to disable isolation mode for ARB.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xe781dba2c807b244ca399bebe5cb3df51a6c7a6c34b33883fcf6237fd7d30e2b](https://etherscan.io/tx/0xe781dba2c807b244ca399bebe5cb3df51a6c7a6c34b33883fcf6237fd7d30e2b)

```
- proposalId: 58
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xd2322f18fbffed420e8edd18efce2309c687820d8730b770b4111557e0850149
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "19" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xd2322f18fbffed420e8edd18efce2309c687820d8730b770b4111557e0850149" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/58.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/58.md)

**Payload reports**

* Arbitrum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/19.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/19.md)

<br>

### Technical analysis

We have verified that the payload modifies the ARB debt ceiling to 0, which means removal of the asset from isolation mode.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
