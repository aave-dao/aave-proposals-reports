# V3. Proposal 13. Aave v3 Ethereum, Polygon, Avalanche, Optimism, Arbitrum, Metis, BNB - USDT risk parameters update

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=13](https://vote.onaave.com/proposal/?proposalId=13)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-harmonize-usdt-risk-parameters-on-aave-v3-markets/15815](https://governance.aave.com/t/arfc-harmonize-usdt-risk-parameters-on-aave-v3-markets/15815)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal harmonises the risk parameters of USDT across the majority of Aave v3 instances, by updating its LTV and LTV. Additionally, the asset is removed from isolation wherever applicable.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x0b3014e4a03a6552db5f9e22ff606478489598cf4ac001cfe2dfc9111ddc7252](https://etherscan.io/tx/0x0b3014e4a03a6552db5f9e22ff606478489598cf4ac001cfe2dfc9111ddc7252)


```
- proposalId: 13
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xfd47bc0dfa38b2b849cebb12d3090a8b58b8b3fbac7915e3e6bfe637c663bdc1
```

**createProposal() parameters**
```
{
  "payloads": [
    {
      "chain": "1",
      "accessLevel": 1,
      "payloadsController": "0xdabad81af85554e9ae636395611c58f7ec1aaec5",
      "payloadId": "53"
    },
    {
      "chain": "137",
      "accessLevel": 1,
      "payloadsController": "0x401b5d0294e23637c18fcc38b1bca814cda2637c",
      "payloadId": "31"
    },
    {
      "chain": "43114",
      "accessLevel": 1,
      "payloadsController": "0x1140cb7cafacc745771c2ea31e7b5c653c5d0b80",
      "payloadId": "13"
    },
    {
      "chain": "10",
      "accessLevel": 1,
      "payloadsController": "0x0e1a3af1f9cc76a62ed31ededca291e63632e7c4",
      "payloadId": "11"
    },
    {
      "chain": "42161",
      "accessLevel": 1,
      "payloadsController": "0x89644ca1bb8064760312ae4f03ea41b05da3637c",
      "payloadId": "10"
    },
    {
      "chain": "1088",
      "accessLevel": 1,
      "payloadsController": "0x2233f8a66a728fba6e1dc95570b25360d07d5524",
      "payloadId": "5"
    },
    {
      "chain": "56",
      "accessLevel": 1,
      "payloadsController": "0xe5ef2dd06755a97e975f7e282f828224f2c3e627",
      "payloadId": "1"
    }
  ],
  "votingPortal": "0x9b24c168d6a76b5459b1d47071a54962a4df36c3",
  "ipfsHash": "0xfd47bc0dfa38b2b849cebb12d3090a8b58b8b3fbac7915e3e6bfe637c663bdc1"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/13.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/13.md)

**Payloads report**

**Ethereum**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/53.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/53.md)

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/53_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/53_forge.md)

<br>

**Polygon**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/31.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/31.md)

<br>

**Avalanche**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/13.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/13.md)

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/13_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/13_forge.md)

<br>

**Optimism**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/11.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/11.md)

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/11_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/11_forge.md)

<br>

**Arbitrum**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/10.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/10.md)

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/10_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/10_forge.md)

<br>

**Metis**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/5_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/5_forge.md)

<br>

**BNB Chain**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/1.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/1.md)

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/1_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/1_forge.md)

<br>

<br>

### Technical analysis

The proposal is composed by 7 payloads, one for each network. We have verified they do the following changes.

**[Ethereum](https://etherscan.io/address/0x54F3899FB8b3156f2372ABE86826Fb919DA7a6ff#code#F1#L16)**

- USDT LTV: 74% -> **77%**
- USDT LT: 76% -> **80%**

<br>

**[Polygon](https://polygonscan.com/address/0x5E2174a1A87AbC9ece9a35e75BC7d88F1f5C9344#code#F1#L15)**

- USDT LTV: 75% -> **77%**
- USDT is removed from isolation.

<br>

**[Avalanche](https://snowtrace.io/address/0xF3A0478e924425668c4f44720aC9242a460391e0/contract/43114/code#F1#L16)**

- USDT LTV: 75% -> **77%**
- USDT LT: 81% -> **80%**

<br>

**[Optimism](https://optimistic.etherscan.io/address/0xEe92C48395442f8b8489f12e626052FbA2faf661#code#F1#L16)**

- USDT LTV: 75% -> **77%**
- USDT is removed from isolation.

<br>

**[Arbitrum](https://arbiscan.io/address/0xE55D0c9909C32951ECC5A346342f8D62F362811c#code#F1#L16)**

- USDT LTV: 75% -> **77%**
- USDT is removed from isolation.

<br>

**[Metis](https://explorer.metis.io/address/0x359927Bc6b46134646eA1B30B486753C0EaeDd08/contract/1088/code)**

- USDT LTV: 75% -> **77%**
- USDT is removed from isolation.

<br>

**[BNB Chain](https://bscscan.com/address/0xCc493B98D43Ff1562b80202dE64FdD10b489Ce17#code)**

- USDT LTV: 75% -> **77%**

<br>

The payloads are consistent with the forum description and Snapshot. Only the changes on USDT on BNB Chain were added post-Snapshot, given that Aave v3 BNB activation happened afterwards.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
