# Proposal 180. May Funding Update part B.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=180](https://vote.onaave.com/proposal/?proposalId=180)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-may-funding-update/17768/2](https://governance.aave.com/t/arfc-may-funding-update/17768/2)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x1fd1d93223Cce5248638023E1F387FF540d6EbEc#code#F1#L55)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal serves as Part B of the May funding update, detailing financial actions aimed at optimizing the financial sustainability of the Aave DAO by migrating assets to Aave v3 and depositing idle Treasury funds to generate yield. Additionally, it includes the payout of bug bounties to incentivize ongoing security improvements within the ecosystem.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x7deb121ba7e856aa54a865453dcea6e152c88ffe964458a53854b8d5f9a23c2a](https://etherscan.io/tx/0x7deb121ba7e856aa54a865453dcea6e152c88ffe964458a53854b8d5f9a23c2a)

```
- proposalId: 180
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x6c08584ec488b99df6c6ddb9bcc156779bd8517f4a7f8f5a68955eca6d63a329
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
      "payloadId": "188" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x6c08584ec488b99df6c6ddb9bcc156779bd8517f4a7f8f5a68955eca6d63a329" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/180.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/180.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/188.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/188.md)

<br>

### Technical analysis

We have verified that the payloads correctly execute the financial actions outlined in the proposal, including the migration of aTokens from Aave v2 to v3 and the deposit of idle assets into Aave v3 on Ethereum. The migration of aUSDT, aDAI, aUSDC, and awETH has been implemented as specified, with exceptions for the retained balances. No discrepancies were found between the declared actions and the implementation. The bug bounty payouts were also validated, and the transfer amounts match the specified values. No inconsistencies or adverse effects were observed in the handling of the aTokens or the payout transactions.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum except the amounts of aEthUSDT, aEthUSDC and the note regarding the Atokens above.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

