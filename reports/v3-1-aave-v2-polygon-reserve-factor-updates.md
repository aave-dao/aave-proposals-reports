# V3. Proposal 0. Aave v2 Polygon - Reserve Factor updates

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=1](https://vote.onaave.com/proposal/?proposalId=1)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937/14](https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937/14)

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

Transaction: [https://etherscan.io/tx/0xd5c3f2e3879fe7b5429df9068877cf41d3e18eeca7a064ce8ba7399bacc86d5d](https://etherscan.io/tx/0xd5c3f2e3879fe7b5429df9068877cf41d3e18eeca7a064ce8ba7399bacc86d5d)


```
- proposalId: 1
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x552721cffc5278357af7de0861cbf8a493488c64ec112cf573b9a33623602b90
```

**createProposal() parameters**
```
{
  "payloads": [
    {
      "chain": "137",
      "accessLevel": 1,
      "payloadsController": "0x401b5d0294e23637c18fcc38b1bca814cda2637c",
      "payloadId": "26"
    }
  ],
  "votingPortal": "0x9b24c168d6a76b5459b1d47071a54962a4df36c3",
  "ipfsHash": "0x552721cffc5278357af7de0861cbf8a493488c64ec112cf573b9a33623602b90"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/1.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/1.md)

**Payloads report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/26.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/26.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://polygonscan.com/address/0x306b131Fe65634e26fd6D7cBc4D7F225C01a5F93#code#F1#L14) properly changes the following Reserve Factors on Aave v2 Polygon:

WMATIC: 76% -> **81%**

WBTC: 90% -> **95%**

USDC: 58% -> **63%**

WETH: 80% -> **85%**

DAI: 56% -> **61%**

USDT: 57% -> **62%**


The proposal payload is consistent with the description in the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
