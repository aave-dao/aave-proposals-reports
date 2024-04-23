# Proposal 83. LayerZero bridge adapter update to V2.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=83](https://vote.onaave.com/proposal/?proposalId=83)

<br>

### Governance forum discussion

[https://governance.aave.com/t/bgd-technical-maintenance-proposals/15274/29](https://governance.aave.com/t/bgd-technical-maintenance-proposals/15274/29)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x3C6918c4BfC002979310935f94C9d61Dd2dec3DB#code#F1#L1)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x0FC812DFB0E5Fc83D9b646f2485F6380232DA584#code#F1#L1)

* Avalanche - [proposal payloads](https://snowscan.xyz/address/0x010466280a5c9173F8fEC1eB385AB4D1E331367E#code#F1#L1)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0xfbFAe7B2b4115843063bd9a5B72E1002671fE9e8#code#F19#L1)

* BNB - [proposal payloads](https://bscscan.com/address/0x69F67c181609edA4d8F25Fe225472b9C8675c76C#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:scroll::small_red_triangle: contract upgrade

<br>

### Context

This proposal updates the LayerZero bridge adapters used on a.DI to connect Ethereum with Polygon, Avalanche, BNB and Gnosis to the new LayerZero V2 version in order to bring the bridge adapters to the up to date version.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x99881b4cbfa49c9681451e6233fe11f738a6f901c40d7d309f6bc60b80e376e2](https://etherscan.io/tx/0x99881b4cbfa49c9681451e6233fe11f738a6f901c40d7d309f6bc60b80e376e2)

```
- proposalId: 83
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0x309c9f0c885674230940e60b2a8e6fba9a226483d9117ba916ef72d4e3bd013f
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
      "payloadId": "105" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "53" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "24" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "13" 
    }, 
    { 
      "chain": "56", 
      "accessLevel": "1", 
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627", 
      "payloadId": "11" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x309c9f0c885674230940e60b2a8e6fba9a226483d9117ba916ef72d4e3bd013f" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/83.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/83.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/105.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/105.md)

* Polygon V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/53.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/53.md)

* Avalanche V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/24.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/24.md)

* Gnosis V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/13.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/13.md)

* BNB V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/11.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/11.md)

<br>

### Technical analysis

We have verified that the payload Updates the LayerZero bridge adapters used to connect between networks to LayerZero V2 with the following values:

- Ethereum: 0x8410d9BD353b420ebA8C48ff1B0518426C280FCC

- Polygon: 0x7FAE7765abB4c8f778d57337bB720d0BC53057e3

- Avalanche: 0x10f02995a399C0dC0FaF29914220E9C1bCdE8640

- Gnosis: 0x9b6f5ef589A3DD08670Dd146C11C4Fb33E04494F

- BNB: 0xa5cc218513305221201f196760E9e64e9D49d98A

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
