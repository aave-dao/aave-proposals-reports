# Proposal 143. ADI Shuffle Update.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=143](https://vote.onaave.com/proposal/?proposalId=143)

<br>

### Governance forum discussion

[https://governance.aave.com/t/bgd-technical-maintenance-proposals/15274/39](https://governance.aave.com/t/bgd-technical-maintenance-proposals/15274/39)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xf50a100F8F60C3dC01a98a15231218accB3150C1#code#F1#L1)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x5056B08129D788344F0BDbA4652E936c24229D9a#code#F1#L1)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xFAb9E283d3bf91Cb7732C869F31D97C9A7D1AEAB/contract/43114/code)

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0x896607f9757B68A5432b8B8f2D79abdC2325d91C#code#F1#L1)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x7ED073d35d8a1c6561102d75FA7aF0752a5ddC6e#code#F1#L1)

* Metis - [proposal payloads](https://explorer.metis.io/address/0x82E898b0CDC997b44C704E42574906136E7B5fAd/contract/1088/code)

* Base - [proposal payloads](https://basescan.org/address/0xc45BB75DB1bF012F9E06192aeA7D338FBe3271D8#code#F1#L1)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x050bE7317a8D015E558E68A99e894375B00Bd723#code#F1#L1)

* Scroll - [proposal payloads](https://scrollscan.com/address/0x97d2bBBe4F87783D33FCabf56481c925C6c897e6#code#F1#L1)

* BNB - [proposal payloads](https://bscscan.com/address/0x0853e4272f8AE9b8Be9439490df8Fb5A5c82DBF0#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

:scroll::small_red_triangle: contract upgrade

<br>

### Context

This proposal update a.DI with the new Shuffle mechanism which introduces a mechanism for, whenever a message needs to be sent, the system chooses pseudo-randomly a sub-set of all the available bridges for that specific path.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xa03341e4209745ac3a5870d22bf71b0bbd01c07a4ba16423bc912df704a833b7](https://etherscan.io/tx/0xa03341e4209745ac3a5870d22bf71b0bbd01c07a4ba16423bc912df704a833b7)

```
- proposalId: 143
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0x6301c2925cb10d90827d617324d06358335f468b733daa23401b62f2cb1f1d4d
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
      "payloadId": "155" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "74" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "45" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "41" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "43" 
    }, 
    { 
      "chain": "1088", 
      "accessLevel": "1", 
      "payloadsController": "0x2233F8A66A728FBa6E1dC95570B25360D07D5524", 
      "payloadId": "21" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "27" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "26" 
    }, 
    { 
      "chain": "534352", 
      "accessLevel": "1", 
      "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE", 
      "payloadId": "18" 
    }, 
    { 
      "chain": "56", 
      "accessLevel": "1", 
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627", 
      "payloadId": "19" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x6301c2925cb10d90827d617324d06358335f468b733daa23401b62f2cb1f1d4d" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/143.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/143.md)

**Payload reports**

* Ethereum - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/155.md)

* Polygon - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/74.md)

* Avalanche - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/45.md)

* Optimism - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/41.md)

* Arbitrum - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/43.md)

* Metis - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/21_forge.md)

* Base - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/27.md)

* Gnosis - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/26.md)

* Scroll - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/18_forge.md)

* BNB - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/19.md)
<br>

### Technical analysis

We have verified that the payloads upgrades a.DI to the contracts which are mentioned in the IPFS and initialize them with the parameters which appear in the IPFS, accept Eth->Pol which should be 3 and Pol->Eth which should be 4. The payload itself is correct and the IPFS and forum are correct accept the part which was mentioned before.

<br>

The proposal is consistent with the description on the governance forum except what is mentioned above.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

