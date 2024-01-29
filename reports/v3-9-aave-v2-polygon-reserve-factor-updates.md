# V3. Proposal 9. Aave v2 Polygon - Reserve Factor updates

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=9](https://vote.onaave.com/proposal/?proposalId=9)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937/15](https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937/15)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal increases the Reserve Factor parameter on multiple Aave v2 Polygon assets, with the objective of incentivising migrations to Aave v3 Polygon.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x5c3f4681294853157bdb34037bfff1b81f0f91c22d8ba9af6728169bb0bd7ddb](https://etherscan.io/tx/0x5c3f4681294853157bdb34037bfff1b81f0f91c22d8ba9af6728169bb0bd7ddb)


```
- proposalId: 9
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x3dffd2f1b7a87a3f44ab31d0da89e5b64a6258468843c4599edd4527a4cd8c3a
```

**createProposal() parameters**
```
{
  "payloads": [
    {
      "chain": "137",
      "accessLevel": 1,
      "payloadsController": "0x401b5d0294e23637c18fcc38b1bca814cda2637c",
      "payloadId": "28"
    }
  ],
  "votingPortal": "0x9b24c168d6a76b5459b1d47071a54962a4df36c3",
  "ipfsHash": "0x3dffd2f1b7a87a3f44ab31d0da89e5b64a6258468843c4599edd4527a4cd8c3a"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/9.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/9.md)

**Payloads report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/28.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/28.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://polygonscan.com/address/0x8c6cd76bEdb22ba5Bd79Fa5eBE47e5D99a22d75A#code#F1#L14) properly changes the following Reserve Factors on Aave v2 Polygon:

WMATIC: 81% -> **86%**

WBTC: 95% -> **99.99%**

USDC: 63% -> **68%**

WETH: 85% -> **90%**

DAI: 61% -> **66%**

BAL: 99% -> **99.99%**

USDT: 62% -> **67%**


The proposal payload is consistent with the description in the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
