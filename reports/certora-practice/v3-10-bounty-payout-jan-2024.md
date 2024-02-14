# Proposal 10. Request for Bounty Payout - January 2024

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=10](https://vote.onaave.com/proposal/?proposalId=10)

<br>

### Governance forum discussion

[https://governance.aave.com/t/bgd-request-for-bounty-payout-january-2024/16378](https://governance.aave.com/t/bgd-request-for-bounty-payout-january-2024/16378)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal is a bounty payment execution for security reports submitted on immunify as per Aave's bug bounty program on immunify.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x85a414e6b338ca1a0a776185df5499097ab259edfbe1ba8d1340136fd786c057](https://etherscan.io/tx/0x85a414e6b338ca1a0a776185df5499097ab259edfbe1ba8d1340136fd786c057)

```
- proposalId: 10
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0x7aecf9ccc292c69084e164b3eaf105de4cfa18e19d3ec749d55cec850c805a13
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
      "payloadId": "49"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0x7aecf9ccc292c69084e164b3eaf105de4cfa18e19d3ec749d55cec850c805a13"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/10.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/10.md)

**Payload reports**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/49.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/49.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xd4f7dc4f63d99b0224cE8c7E2aa81DE8Ca7530ad#code#F1#L34) pays the specified addresses (and no others) with exactly the specified amounts of Aave V2 aUSDC tokens.

0x8689e84af34A18Bc461928aa554a71C649beED89 is being paid 5,000e6 in aUSDC.

0xD122c282499Cb6A76197db2D6ba5170D81C4895f is being paid 10,000e6 in aUSDC.

0x2BC5fFc5De1a83a9e4cDDfA138bAEd516D70414b (immunefi.eth) is being paid 1,000e6 aUSDC.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
