# Proposal 159. Stablecoin IR Curve Amendment.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=159](https://vote.onaave.com/proposal/?proposalId=159)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-stablecoin-ir-curve-amendment-on-aave-v2-and-v3-2024-08-15/18669](https://governance.aave.com/t/arfc-chaos-labs-stablecoin-ir-curve-amendment-on-aave-v2-and-v3-2024-08-15/18669)

<br>

### Payloads

* Ethereum V2 - [proposal payloads](https://etherscan.io/address/0xF01D3312C0ce85FF1CC1023d996d6c19B300CbFf#code)
* Ethereum V3 - [proposal payloads](https://etherscan.io/address/0x26c72D1E40F66cC42A6D4D51F1b6c4692882c444#code)
* Polygon - [proposal payloads](https://polygonscan.com/address/0xBb4f1B3C90E95f596329Dc9b03D6e085f6E7050e#code)
* Avalanche - [proposal payloads](https://snowtrace.io/address/0x82AC7DeF04CDb12609De72E63F40A5571df76ac8/contract/43114/code)
* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0x8912C3A9Fe574818d37a49E29d617fD9833cd2B5#code)
* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x9e3c0fdF879F211fd3e70039CA8a7E092338E231#code)
* Base - [proposal payloads](https://basescan.org/address/0x85E715F22D2DA66b7C6dD76d9774fc4c4AcD610b#code)
* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x6bd088aA0BFa25138F1d4f0ff3D59f329DDC28A7#code)
* Scroll - [proposal payloads](https://gnosisscan.io/address/0x6bd088aA0BFa25138F1d4f0ff3D59f329DDC28A7#code)
* Scroll - [proposal payloads](https://scrollscan.com/address/0xdadC37EFA275a38c981818890a5985538EA554B3#code)
* BNB - [proposal payloads](https://bscscan.com/address/0xbaD3196e2b143f918Cb595f253F03aC7232376Bb#code)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal sets new stablecoin Interest Rate parameters (slope1) across all Aave deployments.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x7ea0ca0520e214cf3fc9da4039a710f3b05efae255100e13b0c02fc33a2c99ab](https://etherscan.io/tx/0x7ea0ca0520e214cf3fc9da4039a710f3b05efae255100e13b0c02fc33a2c99ab)

```
- proposalId: 159
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x576175a4657e2ce79f1c9c41b61ac28609466b7886f4d2c0cd25265fd052d0b3
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
      "payloadId": "167" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "80" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "51" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "46" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "48" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "33" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "29" 
    }, 
    { 
      "chain": "534352", 
      "accessLevel": "1", 
      "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE", 
      "payloadId": "21" 
    }, 
    { 
      "chain": "56", 
      "accessLevel": "1", 
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627", 
      "payloadId": "20" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x576175a4657e2ce79f1c9c41b61ac28609466b7886f4d2c0cd25265fd052d0b3" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/159.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/159.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/167.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/167.md)

* Polygon V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/80.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/80.md)

* Avalanche V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/51.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/51.md)

* Optimism V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/46.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/46.md)

* Arbitrum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/48.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/48.md)

* Base V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/33.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/33.md)

* Gnosis V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/29.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/29.md)

* Scroll V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/21_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/21_forge.md)

* BNB V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/20.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/20.md)

<br>

### Technical analysis

We have verified that the payload changes the slope1 of the specified tokens to 5.5%.


<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
