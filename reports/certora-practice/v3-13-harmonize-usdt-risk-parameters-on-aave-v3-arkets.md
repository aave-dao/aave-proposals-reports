# Proposal 13. Harmonize USDT Risk Parameters on Aave V3 Markets

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=13](https://vote.onaave.com/proposal/?proposalId=13)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-harmonize-usdt-risk-parameters-on-aave-v3-markets/15815](https://governance.aave.com/t/arfc-harmonize-usdt-risk-parameters-on-aave-v3-markets/15815)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x54F3899FB8b3156f2372ABE86826Fb919DA7a6ff#code#F1#L1)

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0xEe92C48395442f8b8489f12e626052FbA2faf661#code#F1#L1)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x5E2174a1A87AbC9ece9a35e75BC7d88F1f5C9344#code#F1#L1)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0xE55D0c9909C32951ECC5A346342f8D62F362811c#code#F1#L1)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xF3A0478e924425668c4f44720aC9242a460391e0/contract/43114/
code#F1#L39)

* Metis - [proposal payloads]()

* BNB - [proposal payloads](https://bscscan.com/address/0xCc493B98D43Ff1562b80202dE64FdD10b489Ce17#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal correlates usdt risk parameters - LTV and LT, across markets and disable isolation mode on several L2 markets.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x0b3014e4a03a6552db5f9e22ff606478489598cf4ac001cfe2dfc9111ddc7252](https://etherscan.io/tx/0x0b3014e4a03a6552db5f9e22ff606478489598cf4ac001cfe2dfc9111ddc7252)

```
- proposalId: 13
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xfd47bc0dfa38b2b849cebb12d3090a8b58b8b3fbac7915e3e6bfe637c663bdc1
```

<br>

**createProposal() parameters**

```
{
  "payloads": [
    {
      "chain": "1",
      "accessLevel": 1,
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
      "payloadId": "53"
    },
    {
      "chain": "137",
      "accessLevel": 1,
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
      "payloadId": "31"
    },
    {
      "chain": "43114",
      "accessLevel": 1,
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
      "payloadId": "13"
    },
    {
      "chain": "10",
      "accessLevel": 1,
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
      "payloadId": "11"
    },
    {
      "chain": "42161",
      "accessLevel": 1,
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
      "payloadId": "10"
    },
    {
      "chain": "1088",
      "accessLevel": 1,
      "payloadsController": "0x2233F8A66A728FBa6E1dC95570B25360D07D5524",
      "payloadId": "5"
    },
    {
      "chain": "56",
      "accessLevel": 1,
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627",
      "payloadId": "1"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0xfd47bc0dfa38b2b849cebb12d3090a8b58b8b3fbac7915e3e6bfe637c663bdc1"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/13.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/13.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/53.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/53.md)

* Optimism - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/11.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/11.md)

* Polygon - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/31.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/31.md)

* Arbitrum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/10.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/10.md)

* Avalanche - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/13.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/13.md)

* Metis - [proposal payloads]()

* BNB - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/1.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/1.md)

<br>

### Technical analysis

We have verified that the payloads modify the LTV and LT of usdt across the specified networks to 77% and 80% respectively, and removes the asset from isolation mode on polygon, optimism and arbitrum.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: The usdt risk parameters across all the stated markets were updated to the mentioned values.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
