# Proposal 132. Aave v3.1 upgrade.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=132](https://vote.onaave.com/proposal/?proposalId=132)

<br>

### Governance forum discussion

[https://governance.aave.com/t/bgd-aave-v3-1-and-aave-origin/17305](https://governance.aave.com/t/bgd-aave-v3-1-and-aave-origin/17305)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x3bf13188225532Dbd685E2c61b78764F97082D7C#code#F1#L1)

* Polygon - [proposal payloads](https://polygonscan.com/address/0xA90ea303522c0df5028687aF2aD6D9231325Abe1#code#F1#L1)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x790B67496cB43b25527451Ff8f954e9198EC9bAb/contract/43114/code)

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0x9F6C2BC9464213b3C71B2b19A80fc3d56a48342F#code#F1#L1)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x9F6C2BC9464213b3C71B2b19A80fc3d56a48342F#code#F1#L1)

* Metis - [proposal payloads](https://explorer.metis.io/address/0x9720ce2Cd5742197D6793723B256282a8920Ed86/contract/1088/code#loaded)

* Base - [proposal payloads](https://basescan.org/address/0x0Ec40C6dA8C7fc6E39BBCe8c6f24c894389a69A7#code#F1#L1)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0xb7F0202604eF32AaAbdD79053a8777e928EdF70E#code#F1#L1)

* Scroll - [proposal payloads](https://scrollscan.com/address/0xa91a89a230568A86FC3E72610baeB0D917453790#code#F1#L1)

* BNB - [proposal payloads](https://bscscan.com/address/0xCa6dFc503f7024CB599Be40628232D74393C5d70#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

:handshake: permission granting or revoking

:scroll::small_red_triangle: contract upgrade

<br>

### Context

This proposal activates Aave v3.1 which is an upgrade to the current v3 on all markets and includes multiple new features.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x423b2b381444d3a8a347536eaf643da3c7bc5e764ff4881863e012305d9542ba](https://etherscan.io/tx/0x423b2b381444d3a8a347536eaf643da3c7bc5e764ff4881863e012305d9542ba)

```
- proposalId: 132
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0x392c2cdfd6c2f57a7be73b170d472b4b8e6c662cb941451b449a0b2988ab3d57
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
      "payloadId": "146" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "71" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "42" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "38" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "39" 
    }, 
    { 
      "chain": "1088", 
      "accessLevel": "1", 
      "payloadsController": "0x2233F8A66A728FBa6E1dC95570B25360D07D5524", 
      "payloadId": "19" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "25" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "23" 
    }, 
    { 
      "chain": "534352", 
      "accessLevel": "1", 
      "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE", 
      "payloadId": "15" 
    }, 
    { 
      "chain": "56", 
      "accessLevel": "1", 
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627", 
      "payloadId": "17" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x392c2cdfd6c2f57a7be73b170d472b4b8e6c662cb941451b449a0b2988ab3d57" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/132.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/132.md)

**Payload reports**

* Ethereum - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/146.md)

* Polygon - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/71.md)

* Avalanche - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/42.md)

* Optimism - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/38.md)

* Arbitrum - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/39.md)

* Metis - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/19_forge.md)

* Base - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/25.md)

* Gnosis - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/23.md)

* Scroll - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/15_forge.md)

* BNB - [proposal payloads](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/17.md)
<br>

### Technical analysis

We have verified that the payload activates v3.1 on all markets with the following:

- The PoolConfigurator implementation is upgraded.

- The Pool implementation is upgraded.

- The Data Provider is upgraded.

- All assets are updated with their most recent value which includes indexes and data rates

- All assets except Ethereum GHO are being enabled to use virtualAccounting and initialized with their current virtualAccounting

- All assets are receiving new intersetRateStrategy address which will be permanent instead of the current method where a new strategy is created each time there is an update to an immutable parameter in it.

- All frozen assets with LTV != 0 will be updated such that the pendingLtv of each one will be updated to the current LTV and the LTV it self to 0.

- On Avalanche the risk admin will be removed temporarily.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

