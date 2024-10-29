# Proposal 193. Aave BGD Phase 4.


<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=193](https://vote.onaave.com/proposal/?proposalId=193)

<br>

### Governance forum discussion

[https://governance.aave.com/t/aave-bored-ghosts-developing-phase-4/19484/7](https://governance.aave.com/t/aave-bored-ghosts-developing-phase-4/19484/7)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x84B910EcaE3c899564CAD4149c4Bd5879CD25a99#code)

<br>

## Certora analysis

<br>

### Proposal types

:bank: payment stream

<br>

### Context

This Proposal for an engagement of development and security services between the Aave DAO and BGD Labs, from 1st October 2024 until 1st April 2025.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x590ceba6615c7890e87eabc7688bd333b081e1e839638a98429e2c22fe73d946](https://etherscan.io/tx/0x590ceba6615c7890e87eabc7688bd333b081e1e839638a98429e2c22fe73d946)

```
- proposalId: 193
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0x0b70648bec071bb3647ec46eebafe02991bc0ff0b0b335ece55cb273b6aadbce
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
      "payloadId": "200" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x0b70648bec071bb3647ec46eebafe02991bc0ff0b0b335ece55cb273b6aadbce" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/193.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/193.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/200.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/200.md)

<br>

### Technical analysis
We have verified that the proposal initiates an upfront transfer of 1,150,000 aUSDC and 2,500 AAVE tokens, followed by a payment stream of equivalent values, covering the specified duration until April 1, 2025, from the Aave DAO's treasury and Ecosystem Reserve as agreed with BGD Labs.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

