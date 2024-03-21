# Proposal 54. Reserve Factor Updates (March 13, 2024).

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=54](https://vote.onaave.com/proposal/?proposalId=54)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937/20](https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937/20)

<br>

### Payloads

* Polygon - [proposal payloads](https://polygonscan.com/address/0xc720DD89B90f760ABc25bd962319EF1709153Dbe#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal increases the reserve factors of multiple assets on Aave-V2-Polygon by 5% up to 99% in order to encouraging users to migrate from Polygon v2 to v3.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x1c9998f964ba0d0e6576c4b377da165bc02d0c1883ff84ba28a1c92387206c2c](https://etherscan.io/tx/0x1c9998f964ba0d0e6576c4b377da165bc02d0c1883ff84ba28a1c92387206c2c)

```
- proposalId: 54
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x93db9bcb9bf20c545d86506c34eee6761adea4bab64bae39290f7466dbf3e56d
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
      "payloadId": "43" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x93db9bcb9bf20c545d86506c34eee6761adea4bab64bae39290f7466dbf3e56d" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/54.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/54.md)

**Payload reports**

* Polygon V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/43.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/43.md)

<br>

### Technical analysis

We have verified that the payload modifies the reserve factor of the following tokens to the following values:

DAI: 86%

USDC: 88%

USDT: 87%

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
