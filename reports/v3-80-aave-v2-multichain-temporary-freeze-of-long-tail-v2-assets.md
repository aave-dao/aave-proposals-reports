# Proposal 80. Temporary Freeze of Long-Tail V2 Assets on Ethereum, Polygon, Avalanche.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=80](https://vote.onaave.com/proposal/?proposalId=80)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-temporary-freeze-of-long-tail-v2-assets/17403](https://governance.aave.com/t/arfc-temporary-freeze-of-long-tail-v2-assets/17403)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x0b3044466f299F3AB771B45cc09B2d00Ff0b2465#code#F1#L1)

* Polygon - [proposal payloads](https://polygonscan.com/address/0xb3cf685FDa5259a510f698B1fe93e49b6C8D523A#code#F1#L1)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xA632ef9CB738f2991Dea7f74013cA20F4f3322a7/contract/43114/code)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal temporary freezes multiple assets on Aave-V2-Ethereum, Aave-V2-Avalanche and Aave-v2-Polygon as part of the v2 deprecation.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xf219b30ead39380cf904e2dfb477f73104dc2245bc40a44dfbb83e6a94b1e420](https://etherscan.io/tx/0xf219b30ead39380cf904e2dfb477f73104dc2245bc40a44dfbb83e6a94b1e420)

```
- proposalId: 80
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xa39d09939ca597beebecad4455a0846a14e2e5af659fe3d8904bda4bc996cf40
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
      "payloadId": "107" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "55" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "26" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xa39d09939ca597beebecad4455a0846a14e2e5af659fe3d8904bda4bc996cf40" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/80.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/80.md)

**Payload reports**

* Ethereum V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/107.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/107.md)

* Polygon V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/55.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/55.md)

* Avalanche V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/26.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/26.md)

<br>

### Technical analysis

We have verified that the payload freezes the following tokens on the following chains:

- Ethereum V2:

    USDP
    
    GUSD
    
    LUSD
    
    FRAX
    
    sUSD
    
    AAVE

- Polygon V2:

    AAVE

- Avalanche V2:

    AAVE

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
