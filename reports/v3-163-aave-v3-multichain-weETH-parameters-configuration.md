# Proposal 163. weETH Parameters Configuration.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=163](https://vote.onaave.com/proposal/?proposalId=163)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-harmonize-weeth-parameters/19012/2](https://governance.aave.com/t/arfc-harmonize-weeth-parameters/19012/2)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x1cd2d6D7851Cb7D6E636AD13315d4B1712b63728#code#F1#L1)
* Arbitrum - [proposal payloads](https://arbiscan.io/address/0xaC9d46d728FF4b8E61ce32110BbaDE37989DBcd7#code#F1#L1) 
* Base - [proposal payloads](https://basescan.org/address/0x7204d840eafF1b9E1621A90Eb4251396FE50320A#code#F1#L1) 
* Scroll - [proposal payloads](https://scrollscan.com/address/0x6949Ef84C8541Df2bE3a532a3DA6666C56e30e5b#code#F1#L1) 



<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal changes and equilize the parameters off weETH across all networks where it is supported. 

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x1331f675307d6f3385bf83dfce05a4cbec386075b668b6ec0236754db2c50347](https://etherscan.io/tx/0x1331f675307d6f3385bf83dfce05a4cbec386075b668b6ec0236754db2c50347)

```
- proposalId: 163
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x04271f18d6488ac110ba7d0faa32b0c9dbb68828585a85a5f52c2da055dcf8c8
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
      "payloadId": "171" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "50" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "35" 
    }, 
    { 
      "chain": "534352", 
      "accessLevel": "1", 
      "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE", 
      "payloadId": "22" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x04271f18d6488ac110ba7d0faa32b0c9dbb68828585a85a5f52c2da055dcf8c8" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/163.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/163.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/171.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/171.md)
* Arbitrum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/421610x89644CA1bB8064760312AE4F03ea41b05dA3637C/50.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/50.md)
* Base - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/35.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/35.md)
* Scroll - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/22_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/22_forge.md)



<br>

### Technical analysis

We have verified that the weETH parametes have been changed properly across all the networks where is supported.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
