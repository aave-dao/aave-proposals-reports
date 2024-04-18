# Proposal 77. Ethereum PYUSD Emission Admin.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=77](https://vote.onaave.com/proposal/?proposalId=77)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-set-aave-chan-initiative-as-emission-manager-for-pyusd-on-aave-v3-ethereum-market/16837](https://governance.aave.com/t/arfc-set-aave-chan-initiative-as-emission-manager-for-pyusd-on-aave-v3-ethereum-market/16837)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xbb5a3cE88358e584c0e2d8FbBb25b5062cCCffe2#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:handshake: permission granting or revoking

<br>

### Context

This proposal propose to set an emission manager for PYUSD on Ethereum chain to incentivize growth of Aave v3 on the Ethereum chain.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x559c69783c7a37f7812f54de205754abee88950f574e48263fc01a0965f98e7f](https://etherscan.io/tx/0x559c69783c7a37f7812f54de205754abee88950f574e48263fc01a0965f98e7f)

```
- proposalId: 77
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x326abb9504b2e2277440be16f89f9f12a17705e4e6a2e098562bf946ff779f1f
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
      "payloadId": "103" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x326abb9504b2e2277440be16f89f9f12a17705e4e6a2e098562bf946ff779f1f" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/77.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/77.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/103.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/103.md)

<br>

### Technical analysis

We have verified that the payload is setting a declared ACI multisig as the emission admin of PYUSD over the Ethereum chain and has no further side effects.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
