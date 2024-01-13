# V3. Proposal 2. Aave v2/v3 Avalanche - Risk parameters update

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=2](https://vote.onaave.com/proposal/?proposalId=2)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-wbtc-e-on-v2-and-v3-avalanche/15824](https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-wbtc-e-on-v2-and-v3-avalanche/15824)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal freezes WBTC.e on both Aave v2 and v3 Avalanche, in order to incentize the migration to BTC.b.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x3b67066fe02ab1a19c13496de00eb016a30eed6466e8df8a5752dcd120b027bb](https://etherscan.io/tx/0x3b67066fe02ab1a19c13496de00eb016a30eed6466e8df8a5752dcd120b027bb)


```
- proposalId: 2
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x7daf1c990ca47b29e121845efc40ac7e4384b70536f2dee46dd06d4e03920d4c
```

**createProposal() parameters**
```
{
  "payloads": [
    {
      "chain": "43114",
      "accessLevel": 1,
      "payloadsController": "0x1140cb7cafacc745771c2ea31e7b5c653c5d0b80",
      "payloadId": "11"
    }
  ],
  "votingPortal": "0x9b24c168d6a76b5459b1d47071a54962a4df36c3",
  "ipfsHash": "0x7daf1c990ca47b29e121845efc40ac7e4384b70536f2dee46dd06d4e03920d4c"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/2.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/2.md)

**Payloads report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/11.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/11.md)

<br>

### Technical analysis

The proposal payload has 2 actions, one for v2 Avalanche and the other to v3. We have verified they do the following:

[v2 Avalanche](https://snowtrace.io/address/0xbd91EEE2F5Db6D94Fbe820A861137227574ebdb5/contract/43114/code#F1#L14)

- It freezes the WBTC.e asset.
- LTV: 60% -> **0%**.
- Liquidation threshold: 75% -> **70%**

<br>

[v3 Avalanche](https://snowtrace.io/address/0xAeA8391726122005dDa7a11f2D2DBA863e53Ec2e/contract/43114/code#F1#L16)

- It freezes the WBTC.e asset.
- LTV: 70% -> **0%**.
- Liquidation threshold: 75% -> **70%**

<br>


The proposal payload is consistent with the description in the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
