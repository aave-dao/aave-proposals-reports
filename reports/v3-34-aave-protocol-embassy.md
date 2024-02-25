# Proposal 34. Aave Protocol Embassy.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=34](https://vote.onaave.com/proposal/?proposalId=34)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-establishing-the-aave-protocol-embassy-ape/16445](https://governance.aave.com/t/arfc-establishing-the-aave-protocol-embassy-ape/16445)

<br>

### Payloads

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x345F46cD52AE631Cd9399F2D15d7F93B52cBE094#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal transfers all available ARB on Aave V3 Arbitrum to the Aave Protocol Embassy multi-sig in order to effectively leverage voting power and actively participate in pivotal governance decisions, such as LTIPs on Arbitrum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x414a0b1bff3a1c3980035b54005c4e199c626faa0320b178b5d9cadf019d35c3](https://etherscan.io/tx/0x414a0b1bff3a1c3980035b54005c4e199c626faa0320b178b5d9cadf019d35c3)

```
- proposalId: 34
- creator: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- accessLevel: 1
- ipfsHash: 0x0417354ab498c7188216a1fde4689346703f3da13c3f19bb5917a11e2db70212
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "11" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x0417354ab498c7188216a1fde4689346703f3da13c3f19bb5917a11e2db70212" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/34.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/34.md)

**Payload reports**

* Arbitrum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/11.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/11.md)

<br>

### Technical analysis

We have verified that the payload transfers all ARB from the collector to the stated safe.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
