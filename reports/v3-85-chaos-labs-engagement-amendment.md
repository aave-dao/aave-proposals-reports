# Proposal 85. Chaos Labs Engagement Amendment.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=85](https://vote.onaave.com/proposal/?proposalId=85)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-engagement-amendment/17324](https://governance.aave.com/t/arfc-chaos-labs-engagement-amendment/17324)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x075d8C4AEC8e3aCc7b3689E064D838ca8bB07E5C#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:bank: payment stream

<br>

### Context

This proposal is an addition of $400,000 to ChaosLabs, bringing their total annual compensation to $2M in order to amend to their current scope of work and compensation structure accordingly.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xea0c8287c0d4b824aaa550c1ee4a5d0ad52dafde7c542270a684c5c29afdfa0e](https://etherscan.io/tx/0xea0c8287c0d4b824aaa550c1ee4a5d0ad52dafde7c542270a684c5c29afdfa0e)

```
- proposalId: 85
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xc3933570aa757db7e941c51b9bf486f0cf17bcb38c1b95a9293fde7f5118259c
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
      "payloadId": "109" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xc3933570aa757db7e941c51b9bf486f0cf17bcb38c1b95a9293fde7f5118259c" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/85.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/85.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/109.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/109.md)

<br>

### Technical analysis

We have verified that the following payments were made to the address provided by ChaosLabs.

Stream to the benefit of ChaosLabs:
- 400,000 GHO streamed until their current scope ends, starting at execution, roughly around 200 days. 

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
