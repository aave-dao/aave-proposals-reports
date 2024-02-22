# Proposal 30. Reserve Factor Updates (February 15, 2024).

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=30](https://vote.onaave.com/proposal/?proposalId=30)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937/17](https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937/17)

<br>

### Payloads

* Polygon - [proposal payloads](https://polygonscan.com/address/0x4230bB3D21D1bDd5fBE568969A086e5A38882D7e#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal increases the reserve factors of the following assets on Aave-V2-Polygon by 5% up to 99%: DAI, USDC, USDT, wETH, MATIC, in order to reduce deposit yield on Polygon v2 encouraging people to migrate from Polygon v2 to v3.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xd7254af55a4a6761886a9e36128925d7a4ea633d956b8aef54707dc4af65dc8c](https://etherscan.io/tx/0xd7254af55a4a6761886a9e36128925d7a4ea633d956b8aef54707dc4af65dc8c)

```
- proposalId: 30
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x88e32b5864330954e2f464205f8103f1b4e4f263165339b78820ce5031524201
```

<br>

**createProposal() parameters**

```
{
  "payloads": [
    {
      "chain": "137",
      "accessLevel": 1,
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
      "payloadId": "36"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0x88e32b5864330954e2f464205f8103f1b4e4f263165339b78820ce5031524201"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/30.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/30.md)

**Payload reports**

* Polygon V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/36.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/36.md)

<br>

### Technical analysis

We have verified that the payload modifies the reserve factor of the following tokens:

DAI: 76%

USDC: 78%

USDT: 77%

wETH: 99.99%

MATIC: 96%

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
