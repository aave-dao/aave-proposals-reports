# Proposal 136. Events Grant 2024.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=136](https://vote.onaave.com/proposal/?proposalId=136)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-aave-events-sponsorship-proposal-2024/18276](https://governance.aave.com/t/arfc-aave-events-sponsorship-proposal-2024/18276)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x02303770744906B1401f84920241D3d3896fA93F#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal is a budget allocation of 650,000 GHO for events at key ecosystem initiatives which are aimed at helping to continue the expansion of the DeFi ecosystem by showcasing Aave Protocol’s core values.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x6c5b76507fc3e58799b0b0f1efdc8f6ee6e31fd13e3f6f02dc6270ecb367f753](https://etherscan.io/tx/0x6c5b76507fc3e58799b0b0f1efdc8f6ee6e31fd13e3f6f02dc6270ecb367f753)

```
- proposalId: 136
- creator: 0x66a28531e6f390a8cd44ab0c57a0f1aeb7e673ff
- accessLevel: 1
- ipfsHash: 0xf201622bcd8e4bf3b959c99eb343486b34aabe27e60bdcdef43a9f60af191541
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
      "payloadId": "150" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xf201622bcd8e4bf3b959c99eb343486b34aabe27e60bdcdef43a9f60af191541" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/136.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/136.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/150.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/150.md)

<br>

### Technical analysis

We have verified that the payload transfers 650,000 GHO to Aave Labs declared address. 

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

