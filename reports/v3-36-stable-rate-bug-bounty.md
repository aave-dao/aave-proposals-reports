# Proposal 36. Stable Rate Bug Bounty.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=36](https://vote.onaave.com/proposal/?proposalId=36)

<br>

### Governance forum discussion

[https://governance.aave.com/t/bgd-full-deprecation-of-stable-rate/16473](https://governance.aave.com/t/bgd-full-deprecation-of-stable-rate/16473)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x0EbC54096B3f822D804e0280fa71c026EbbD4DA6#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal is a bounty payment execution for a critical security report submitted by a white hat.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x509911024426e33c6c6ec7e5a4f8fd995423786ec8eb47100c15b17d90d7350e](https://etherscan.io/tx/0x509911024426e33c6c6ec7e5a4f8fd995423786ec8eb47100c15b17d90d7350e)

```
- proposalId: 36
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0xaab715c2dcc34b8c5a9cd408f6b42c1d3b319c857885f3fc5d9083874f53ef95
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
      "payloadId": "66" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xaab715c2dcc34b8c5a9cd408f6b42c1d3b319c857885f3fc5d9083874f53ef95" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/36.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/36.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/66.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/66.md)

<br>

### Technical analysis

We have verified that the payload transfers 500,000 aUSDT-v2-Ethereum from the Aave Ethereum Collector, 5'583 AAVE from the Aave eco reserve system to the white hat and 100,000 aUSDT-v2-Ethereum from the Aave Ethereum Collector to immunify - the 10% fee.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
