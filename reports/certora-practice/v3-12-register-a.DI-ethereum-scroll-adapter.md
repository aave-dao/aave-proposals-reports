# Proposal 12. Register a.DI Ethereum -> Scroll adapter

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=12](https://vote.onaave.com/proposal/?proposalId=12)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-aave-v3-deployment-on-scroll-mainnet/16126](https://governance.aave.com/t/arfc-aave-v3-deployment-on-scroll-mainnet/16126)

<br>

### Payloads

* Ethereum V3 - [https://etherscan.io/address/0x2FF5270d6092bA8718Ef00fa1304bC2De9b8047F#code#F1#L1](https://etherscan.io/address/0x2FF5270d6092bA8718Ef00fa1304bC2De9b8047F#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:handshake: permission granting or revoking

<br>

### Context

This proposal registers an a.DI adapter from Ethereum to Scroll network in order to enable participation of the market in Aave governance.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x0953624defa1191ae479888931ac174c8adacace5598d8cc5ab7002a9aab796b](https://etherscan.io/tx/0x0953624defa1191ae479888931ac174c8adacace5598d8cc5ab7002a9aab796b)

```
- proposalId: 12
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0x589222e8d46e0cabcbf3d7cc79e9f1d60771dfaaa07d0966815a7b35320451b7
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
      "payloadId": "51"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0x589222e8d46e0cabcbf3d7cc79e9f1d60771dfaaa07d0966815a7b35320451b7"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/12.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/12.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/51.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/51.md)

<br>

### Technical analysis

We have verified that the payload registers a bridge adapter from Ethereum to Scroll on the Ethereum V3 cross-chain controller

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
