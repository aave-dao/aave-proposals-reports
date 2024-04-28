# Proposal 87. Risk Parameters for DAI Update.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=87](https://vote.onaave.com/proposal/?proposalId=87)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-risk-parameters-for-dai-update/17211](https://governance.aave.com/t/arfc-risk-parameters-for-dai-update/17211)

<br>

### Payloads

* Ethereum V2- [proposal payloads](https://etherscan.io/address/0xA761FA68173378D0a138A764FB610AbE128545D0#code#F1#L1)

* Ethereum V3- [proposal payloads](https://etherscan.io/address/0xdC3f8a2969675aB03d82369a074B0cc86B052eBb#code#F1#L1)

* Polygon V2- [proposal payloads](https://polygonscan.com/address/0xAF884cac514da5eF833C9Ab49574AA71E5E122fd#code#F1#L1)

* Polygon V3- [proposal payloads](https://polygonscan.com/address/0x517D826A67581826e7a5ED848B23156c467d3Aa1#code#F1#L1)

* Avalanche V2- [proposal payloads](https://snowscan.xyz/address/0x0824D34F3dbc1412BceA272131A15025030D84cA#code#F1#L1)

* Avalanche V3- [proposal payloads](https://snowscan.xyz/address/0xA400923ad6ef8884ecA052E08661E8161c6ad99c#code#F1#L1)

* Optimism V3- [proposal payloads](https://optimistic.etherscan.io/address/0xD1F5433E094cA4C247A578C079b6602e0879DF71#code#F1#L1)

* Arbitrum V3- [proposal payloads](https://arbiscan.io/address/0xc71d91CCB53372c95E7B54548f13cA9ecad0ed38#code#F29#L1)

* Metis V3- [proposal payloads](https://explorer.metis.io/address/0xDC4ad6b65963f8c45811aA514Effb50c10EdE708/contract/1088/code)

* Gnosis V3- [proposal payloads](https://gnosisscan.io/address/0xfd3D1840eb04b5077C3A7465fE1a8107E46318c4#code#F29#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal decreases the liquidation threshold and the LTV of DAI, sDAI on Aave-V3 and Aave-V2 chains due to concerns regarding the inherent risk nature of DAI as collateral.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xf860b15d7ee9fe15d3c6a75f50c280583ca2cc95382ef4cffe34d0a7e54b6364](https://etherscan.io/tx/0xf860b15d7ee9fe15d3c6a75f50c280583ca2cc95382ef4cffe34d0a7e54b6364)

```
- proposalId: 87
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xf5dd9c4b10ba88e184eec2ae80e8ec338f0b11ad48a0ff920119fbf1592115a7
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "1", 
      "accessLevel": "1", 
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5", 
      "payloadId": "112" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "58" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "29" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "28" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "26" 
    }, 
    { 
      "chain": "1088", 
      "accessLevel": "1", 
      "payloadsController": "0x2233F8A66A728FBa6E1dC95570B25360D07D5524", 
      "payloadId": "17" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "15" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xf5dd9c4b10ba88e184eec2ae80e8ec338f0b11ad48a0ff920119fbf1592115a7" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/87.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/87.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/112.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/112.md)

* Polygon - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/58.md](hhttps://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/58.md)

* Avalanche - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/29.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/29.md)

* Optimism - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/28.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/28.md)

* Arbitrum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/26.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/26.md)

* Metis - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/17_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/17_forge.md)

* Gnosis - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/15.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/15.md)


<br>

### Technical analysis

We have verified that the payload decreases the liquidation threshold and the LTV of DAI, sDAI to the following parameters on all chains:

    LTV: 63%

    LT: 77%

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
