# Proposal 41. Reserve Factor Updates (February 29, 2024)

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=41](https://vote.onaave.com/proposal/?proposalId=41)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937/17](https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937/17)

<br>

### Payloads

* Polygon - [proposal payloads](https://polygonscan.com/address/0x408661966C964042bb69b8aF18664e4507E7042d#code#F1#L1)

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

Transaction: [https://etherscan.io/tx/0x2055872699665c1d35c8dcbc251a0747f4bf1ebde05f331dce5f201a992d0ea9](https://etherscan.io/tx/0x2055872699665c1d35c8dcbc251a0747f4bf1ebde05f331dce5f201a992d0ea9)

```
- proposalId: 41
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x65de3c96f0d171e2fa490c180d4aee2a7c057bd9a2e70f7549cdd201efdac409
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
      "payloadId": "39" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x65de3c96f0d171e2fa490c180d4aee2a7c057bd9a2e70f7549cdd201efdac409" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/41.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/41.md)

**Payload reports**

* Polygon V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/39.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/39.md)

<br>

### Technical analysis

We have verified that the payload modifies the reserve factor of the following tokens to the following values:

DAI: 81%

USDC: 83%

USDT: 82%

MATIC: 99.99%

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
