# Proposal 38. Cut Gauntlet Service Provider Stream.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=38](https://vote.onaave.com/proposal/?proposalId=38)

<br>

### Governance forum discussion

[https://governance.aave.com/t/gauntlet-is-leaving-aave/16700](https://governance.aave.com/t/gauntlet-is-leaving-aave/16700)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xB84Fdbd7be151A1847DdDdca5966c597b989Cd38#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:bank: payment stream

<br>

### Context

This proposal cancels the payment streams of Gauntlet as they are leaving Aave Service providers.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xcf5ae88c1e8e06aba46e407a01ab96b8e68cc828c8746f778ad3b9ee31d4a6b8](https://etherscan.io/tx/0xcf5ae88c1e8e06aba46e407a01ab96b8e68cc828c8746f778ad3b9ee31d4a6b8)

```
- proposalId: 38
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x447462045acf250a9edb3c52a52d4d5a39b3f47074752e14f02450ce72aa7d64
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
      "payloadId": "68" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x447462045acf250a9edb3c52a52d4d5a39b3f47074752e14f02450ce72aa7d64" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/38.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/38.md)

**Payload reports**

* Ethereum V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/68.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/68.md)

<br>

### Technical analysis

We have verified that the payload cancels the following payment streams:

- stream 100021 for aUSDT.

- stream 100022 for GHO.
<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
