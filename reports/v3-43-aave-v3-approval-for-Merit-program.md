# Proposal 43. Merit Approvals

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=43](https://vote.onaave.com/proposal/?proposalId=43)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-merit-a-new-aave-alignment-user-reward-system/16646/31](https://governance.aave.com/t/arfc-merit-a-new-aave-alignment-user-reward-system/16646/31)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x93236aA0AA30DE7f837D0BAD24663303a9e852B8#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal approves a SAFE multisig wallet dedicated for the Merit program with funds to be distributed with protocol aligned users, as described and elaborated on in the forum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xaf882e47dd2c17638164b3570447a8ed60e77114ee0c1208ae7d7839fa3eadaa](https://etherscan.io/tx/0xaf882e47dd2c17638164b3570447a8ed60e77114ee0c1208ae7d7839fa3eadaa)

```
- proposalId: 43
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xb237c4f579095dc1830ff7ccdbfa69a30b0c1afa302d9ade1faa19f2684a0b7a
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
      "payloadId": "72" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xb237c4f579095dc1830ff7ccdbfa69a30b0c1afa302d9ade1faa19f2684a0b7a" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/43.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/43.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/72.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/72.md)

<br>

### Technical analysis

We have verified that the payload approves exactly 2.9M GHO and 600 aWETH from the collector to the specified Merit SAFE wallet.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
