# Proposal 59. Aave BGD Phase 3.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=59](https://vote.onaave.com/proposal/?proposalId=59)

<br>

### Governance forum discussion

[https://governance.aave.com/t/aave-bored-ghosts-developing-phase-3/16893](https://governance.aave.com/t/aave-bored-ghosts-developing-phase-3/16893)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x97B53cD563DA629640F55821189452315c05F177#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal offers the DAO a new engagement with BGD Labs for further maintenance of the Aave protocol as well as new development.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xbb4e90afac0b7b6749793f22817abb2325414c3c08e13f89d091a6e9876571cc](https://etherscan.io/tx/0xbb4e90afac0b7b6749793f22817abb2325414c3c08e13f89d091a6e9876571cc)

```
- proposalId: 59
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0xa90b3bf86207fa4b298c36eb83cc9b617ec9308a0663eda73605f09319a5bc2b
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
      "payloadId": "87" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xa90b3bf86207fa4b298c36eb83cc9b617ec9308a0663eda73605f09319a5bc2b" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/59.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/59.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/87.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/87.md)

<br>

### Technical analysis

We have verified that the following payments were made to the address provided by BGD.

Direct transfer from the collector to BGD Lab's wallet:
- 6,000 AAVE from the ecosystem reserve controller.
- 960,000 aUSDT from the Aave V2 collector.
- 760,000 aUSDC from the Aave V3 collector.

Streams to the benefit of BGD Lab:
- 2,000 AAVE for scope 1 streamed over a period of 180 days, starting at execution. 
- 640,000 GHO for scope 1 streamed over a period of 180 days, starting at execution.
- 4,500 AAVE for scope 2 streamed over a period of 1 second, starting exactly 120 days from execution.
- 1,140,000 Aave V3 aUSDC for scope 2 streamed over a period of 1 second, starting exactly 120 days from execution.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
