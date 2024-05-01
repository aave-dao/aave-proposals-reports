# Proposal 92. Hyperlane bridge adapter update to V3.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=92](https://vote.onaave.com/proposal/?proposalId=92)

<br>

### Governance forum discussion

[https://governance.aave.com/t/bgd-technical-maintenance-proposals/15274/31](https://governance.aave.com/t/bgd-technical-maintenance-proposals/15274/31)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x6F829BC776eDc377fb12049A5229Ab5EF0D09885#code#F1#L1)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x9f21A46Cd0c789d46174C919044d9AeF914f96F9#code#F1#L1)

* Avalanche - [proposal payloads](https://snowscan.xyz/address/0x0a54a0c111e00cd9D0181b9285591164ba41b6FA#code#F1#L1)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x08163cA0B450D1AE967AD30dA4FAC637B3b19014#code#F1#L1)

* BNB - [proposal payloads](https://bscscan.com/address/0xab69Ac296FeF08FaFF7405843d90aA08F1E79642#code#F1#L1)

* Scroll - [proposal payloads](https://scrollscan.com/address/0xD5746E84ba79c01e5d05b6ab7a1099159A2Dd4e5#code#F1#L1)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x4DEC035Ab33Df6cD6AB94AC58026C2b1801840F0#code#F1#L1)

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0xAcc89539E5FB4aB5396a745af0E3445E98dF2086#code#F1#L1)

* Metis - [proposal payloads](https://andromeda-explorer.metis.io/address/0xDa79E6CD5713DF19a19bf8f6a6C4e8c2C6d44717?tab=contract)

* Base - [proposal payloads](https://basescan.org/address/0x50C3Cb80c56563eCb46b88D88D3Aa6B3A3Efd16D#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:scroll::small_red_triangle: contract upgrade

<br>

### Context

This proposal updates the Hyperlane bridge adapters used on a.DI to connect Ethereum with Polygon, Avalanche, BNB and Gnosis to the new Hyperlane V3 version in order to bring the bridge adapters to the up to date version. The proposal also removes old native bridges on Optimism, Base, Arbitrum, Scroll and Metis, after verifying that the new active versions work properly.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xe1d55c49b2fd1c88d054abcb7af5ee1d444570d23cf54e54ced9f151a28fa03e](https://etherscan.io/tx/0xe1d55c49b2fd1c88d054abcb7af5ee1d444570d23cf54e54ced9f151a28fa03e)

```
- proposalId: 92
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0xb1cc692a9f2bed0923862de7ff7e603805f38b1b9da844a9977db9dec966b93e
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
      "payloadId": "110" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "56" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "27" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "14" 
    }, 
    { 
      "chain": "56", 
      "accessLevel": "1", 
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627", 
      "payloadId": "12" 
    }, 
    { 
      "chain": "534352", 
      "accessLevel": "1", 
      "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE", 
      "payloadId": "10" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "25" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "27" 
    }, 
    { 
      "chain": "1088", 
      "accessLevel": "1", 
      "payloadsController": "0x2233F8A66A728FBa6E1dC95570B25360D07D5524", 
      "payloadId": "16" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "17" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xb1cc692a9f2bed0923862de7ff7e603805f38b1b9da844a9977db9dec966b93e" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/92.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/92.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/110.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/110.md)

* Polygon - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/56.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/56.md)

* Avalanche - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/27.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/27.md)

* Gnosis - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/14.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/14.md)

* BNB - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/12.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/12.md)

* Scroll - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/10_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/10_forge.md)

* Arbitrum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/25.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/25.md)

* Optimism - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/27.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/27.md)

* Metis - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/16_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/16_forge.md)

* Base - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/17.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/17.md)
<br>

### Technical analysis

We have verified that the payload Updates the Hyperlane bridge adapters used to connect between networks to Hyperlane V3 with the following values:

- Ethereum: 0x01dcb90Cf13b82Cde4A0BAcC655585a83Af3cCC1

- Polygon: 0x3e72665008dC237bdd91C04C10782Ed1987a4019

- Avalanche: 0x617332a777780F546261247F621051d0b98975Eb

- Gnosis: 0xA806DA549FcB2B4912a7dFFE4c1aA7A1ed0Bd5C9

- BNB: 0x3F006299eC88985c18E6e885EeA29A49eC579882

We have also verified that the payload removes the old native receiver bridge adapters:

- Arbitrum: 0x3829943c53F2d00e20B58475aF19716724bF90Ba

- Base: 0x7b62461a3570c6AC8a9f8330421576e417B71EE7

- Metis: 0x746c675dAB49Bcd5BB9Dc85161f2d7Eb435009bf

- Optimism: 0x81d32B36380e6266e1BDd490eAC56cdB300afBe0

- Scroll: 0x118DFD5418890c0332042ab05173Db4A2C1d283c

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
