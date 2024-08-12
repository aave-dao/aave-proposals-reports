# Proposal 148. Register ZKSync adapters on a.DI.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=148](https://vote.onaave.com/proposal/?proposalId=148)

<br>

### Governance forum discussion

[https://governance.aave.com/t/bgd-technical-maintenance-proposals/15274/40](https://governance.aave.com/t/bgd-technical-maintenance-proposals/15274/40)

<br>

### Payloads

* Ethereum - [proposal payload](https://etherscan.io/address/0x65Cf9DE21c5F4377BF7E4d1421cEde57d9D5962A#code)

<br>

## Certora analysis

<br>

### Proposal types

:handshake: permission granting or revoking

<br>

### Context

This proposal adds new bridge adapters for Ethereum -> ZKSync.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x258915c7b2c4fc7da11f009ad0313cea51be9040c0bbee8475fca3f2df38809b](https://etherscan.io/tx/0x258915c7b2c4fc7da11f009ad0313cea51be9040c0bbee8475fca3f2df38809b)

```
- proposalId: 148
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0x66685f33f6f383548a450f539300fea0566272b9e63ce7438a011914f10475ce
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
      "payloadId": "160" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x66685f33f6f383548a450f539300fea0566272b9e63ce7438a011914f10475ce" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/148.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/148.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/160.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/160.md)

<br>

### Technical analysis

We verified that the payload is adding the declared bridge adapters on Ethereum for the ZKSync network in the correct role - forwarder as described in the IPFS.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
