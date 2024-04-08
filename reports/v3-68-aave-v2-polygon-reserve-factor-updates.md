# Proposal 68. Reserve Factor Updates (April 5, 2024).

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=68](https://vote.onaave.com/proposal/?proposalId=68)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937/21](https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937/21)

<br>

### Payloads

* Polygon - [proposal payloads](https://polygonscan.com/address/0x3A19355679Aa122016cd23de2fAeEb2c8f4C8d64#code#F1#L1)

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

Transaction: [https://etherscan.io/tx/0x5e0e6ead265a9594e4cbd5cbe881c4ac4c53ae3b2a8fd294b5464eb74722950c](https://etherscan.io/tx/0x5e0e6ead265a9594e4cbd5cbe881c4ac4c53ae3b2a8fd294b5464eb74722950c)

```
- proposalId: 68
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xa065b0072d967b744ef82f22ef4809258572148c1e31d9a0aef854f8fbdebb12
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
      "payloadId": "47" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xa065b0072d967b744ef82f22ef4809258572148c1e31d9a0aef854f8fbdebb12" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/68.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/68.md)

**Payload reports**

* Polygon V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/47.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/47.md)

<br>

### Technical analysis

We have verified that the payload modifies the reserve factor of the following tokens to the following values:

DAI: 91%

USDC: 93%

USDT: 92%

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
