# Proposal 211. Fluid Alignment


<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=211](https://vote.onaave.com/proposal/?proposalId=211)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-fluid-alignment-with-inst-purchase/19921](https://governance.aave.com/t/arfc-fluid-alignment-with-inst-purchase/19921)

<br>

### Payloads

* Ethereum add flash borrower - [proposal payloads](https://etherscan.io/address/0x122791Ed2e661AEe330BF3b7ff2a0BE844291e59#code)

* Ethereum transfe tokens - [proposal payloads](https://etherscan.io/address/0x5aAB359DFc04577C785337BB5b97beD2Fb407DED#code)

* Ethereum Lido add flash borrower - [proposal payloads](https://etherscan.io/address/0xa4055EB158A7Efe96D13977a41cE638Da28E4f58#code)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x6ddDcDBec097DC9d675cC402dF5a2877Ec70ecD3#code)

* Base - [proposal payloads](https://basescan.org/address/0x5c1736e337A8C657f14EEa9ecC759fDBdC1c54D1#code)


<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

:handshake: permission granting or revoking

<br>

### Context

This proposal aims to strengthen the strategic partnership between Aave DAO and Instadapp through a $4M investment in INST tokens at a $350M fully diluted valuation (FDV). Instadapp has been a key player in the Aave ecosystem, offering essential infrastructure and user interfaces, and their upcoming tokenomics reform and rebranding present a timely opportunity for deeper collaboration. By aligning both protocols, the proposal seeks to promote GHO adoption, prioritize Aave protocol integrations, and create mutual governance value. This initiative also ensures Aave DAO’s active participation in Instadapp’s governance and ecosystem development, further solidifying their collaboration.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x8fb418891365f7094ff885be5f415de126e052d34eee3f7eb89dbc10ce2f050c](https://etherscan.io/tx/0x8fb418891365f7094ff885be5f415de126e052d34eee3f7eb89dbc10ce2f050c)

```
- proposalId: 211
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x5018fc573e6e6d8534f44ca40d8b1e0c0c38a60595037d3d059b840ea6523a59
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
      "payloadId": "215" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "64" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "46" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x5018fc573e6e6d8534f44ca40d8b1e0c0c38a60595037d3d059b840ea6523a59" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/211.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/211.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/215.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/215.md)

* Arbitrum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/64.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/64.md)

* Base - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/46.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/46.md)

<br>

### Technical analysis

We have verified that the flashBorrower role has been correctly granted. Additionally, the transfer mechanics for the $INST token purchase have been thoroughly reviewed, ensuring accurate handling of the decimal numbers. All contract interactions and logic have been audited to confirm alignment with the intended proposal specifications, guaranteeing that the execution meets the outlined requirements without discrepancies.




<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

