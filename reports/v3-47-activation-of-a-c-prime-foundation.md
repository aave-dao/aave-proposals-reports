# Proposal 47. Activation of A-C Prime Foundation.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=47](https://vote.onaave.com/proposal/?proposalId=47)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-aave-treasury-rwa-allocation/14790](https://governance.aave.com/t/arfc-aave-treasury-rwa-allocation/14790)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xA80d2B17680e371405878B2d0fc1Df9853807f1E#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:handshake: Event Emission As Engagement Proof

<br>

### Context

This proposal proposes the activation of the A-C Prime Foundation which is an Association to represent the Aave DAO off-chain. THis proposal does not require any on-chain changes and simply emits an event which approves the activision.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xfa2a20615e1ff91d9fcb4cd4f5dd5488f41ec6b762d0e9ebbc9b04038db1bb37](https://etherscan.io/tx/0xfa2a20615e1ff91d9fcb4cd4f5dd5488f41ec6b762d0e9ebbc9b04038db1bb37)

```
- proposalId: 47
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x8d80f7e09630024192366b533cc95274f37d3d3e0d3d004aa5eb7b637f1be113
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
      "payloadId": "77" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x8d80f7e09630024192366b533cc95274f37d3d3e0d3d004aa5eb7b637f1be113" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/47.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/47.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/77.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/77.md)

<br>

### Technical analysis

We have verified that the payload emits an event with a message approving the activision of the A-C Prime Foundation.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
