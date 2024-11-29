# Proposal 208. Upadte Flash Borrowers addresses across various instances of Aave v3.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=208](https://vote.onaave.com/proposal/?proposalId=208)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-add-dhedge-protocol-to-flashborrowers/19547](https://governance.aave.com/t/arfc-add-dhedge-protocol-to-flashborrowers/19547)

<br>

### Payloads

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0x5Adb12a121cD50670A7E18744275A008387be21e#code)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x772e2A90a97D05692214463A3AeB1038436B8dB7#code)

* Base - [proposal payloads](https://basescan.org/address/0x03Ca803F0598da57739a0D96aD39c9e1d5a0393F#code)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x7ee9d11837269D8DC300e09E17066a0591E7dcbD#code)


<br>

## Certora analysis

<br>

### Proposal types

:handshake: permission granting or revoking

<br>

### Context

This proposal updates updates whitelisted flashBorrowers addresses across various instances of Aave v3.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x9f77d4ae4b29bfffe51cb6668fa87ee604ae854575552f122882faba80ba93bf](https://etherscan.io/tx/0x9f77d4ae4b29bfffe51cb6668fa87ee604ae854575552f122882faba80ba93bf)

```
- proposalId: 208
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x7e9c183accaccede6def81bd44fd829bec4b43814516bfe8dfef0b27f7f300a6
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "90" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "58" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "62" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "45" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x7e9c183accaccede6def81bd44fd829bec4b43814516bfe8dfef0b27f7f300a6" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/208.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/208.md)

**Payload reports**

* Base - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/45.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/45.md)

* Polygon - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/90.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/90.md)

* Optimism - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/58.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/58.md)

* Arbitrum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/62.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/62.md)


<br>

### Technical analysis

We have verified that the code correctly adds the specified flash borrowers to the Aave V3 ACL managers on the appropriate networks and instances as requested.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
