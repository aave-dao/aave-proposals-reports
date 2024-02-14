# Proposal 9. Reserve Factor Updates (Jan 15, 2024)

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=9](https://vote.onaave.com/proposal/?proposalId=9)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937/14](https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937/14)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

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

<br>

**createProposal() parameters**
```
{
  "payloads": [
    {
      "chain": "137",
      "accessLevel": 1,
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
      "payloadId": "48"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0x3dffd2f1b7a87a3f44ab31d0da89e5b64a6258468843c4599edd4527a4cd8c3a"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/9.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/9.md)

**Payload reports**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/28.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/28.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://polygonscan.com/address/0x8c6cd76bEdb22ba5Bd79Fa5eBE47e5D99a22d75A#code) properly changes the following Reserve Factors on Aave v2 Polygon:

DAI: 61% -> **66_00%**

USDC: 63% -> **68_00%**

USDT: 62% -> **67_00%**

WBTC: 95% -> **99_99%**

WETH: 85% -> **90_00%**

WMATIC: 81% -> **86_00%**

BAL: 99% -> **99_99%**

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: All the stated tokens were updated to the declared values.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
