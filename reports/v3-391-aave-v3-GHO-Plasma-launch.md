# Proposal 391. Gho Plasma Launch

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=391)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-launch-gho-on-plasma-set-aci-as-emissions-manager-for-rewards/22994)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xd7c7F69ca01654fc382531A0F39E83db4318a61C)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x7e426E3f08b30a162A81744BD2E878c3A2ebD977)

* Base - [proposal payloads](https://basescan.org/address/0x5bF824E29D83BA9f9b90CbA74EBdA0884265Ab6C)

* Avalanche - [proposal payloads](https://snowscan.xyz/address/0x3bc588EaF6F12C4CFe5f26849a4107D59f33e45F)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x14C6267470FbeC18e02Ef642630c688AF282Cf0c)

* Ink - [proposal payloads](https://explorer.inkonchain.com/address/0xF433946bD4205e29de77c8e251E0D5e1f16d54c5)

* Plasma - [proposal payloads](https://plasmascan.to/address/0x0bF84870529c17ea618c9e877cfb8379B36aD659)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates

* :handshake: Permission granting and revoking

* :gem: :new: Listing new assets


### Context
This AIP proposes deploying GHO on the Plasma blockchain. The goal is to establish GHO as a key stablecoin within Plasma’s ecosystem from inception, facilitating reward programs, liquidity incentives, and seamless integration with the Aave deployment on Plasma.

### Proposal Creation
Transaction: [0xb83c3c3590451256fbf3dae1aa655141e9967996ff6c2f3f53dcc17a842c3145](https://etherscan.io/tx/0xb83c3c3590451256fbf3dae1aa655141e9967996ff6c2f3f53dcc17a842c3145)
- `proposalId`: 391
- `creator`: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x0dbe5772b9a4cba9cbff4ff607c8de2ceaa11f6af7522427f7a1119baeb3b9c5

**`createProposal()` Parameters**
```
{
  "payloads": [ 
    { 
      "chain": "1", 
      "accessLevel": "1", 
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5", 
      "payloadId": "359" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "105" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "88" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "99" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "64" 
    }, 
    { 
      "chain": "57073", 
      "accessLevel": "1", 
      "payloadsController": "0x44D73D7C4b2f98F426Bf8B5e87628d9eE38ef0Cf", 
      "payloadId": "2" 
    }, 
    { 
      "chain": "9745", 
      "accessLevel": "1", 
      "payloadsController": "0xe76EB348E65eF163d85ce282125FF5a7F5712A1d", 
      "payloadId": "2" 
    }, 
  ], 
  "votingPortal": "0x9Ded9406f088C10621BE628EEFf40c1DF396c172", 
  "ipfsHash": "0x0dbe5772b9a4cba9cbff4ff607c8de2ceaa11f6af7522427f7a1119baeb3b9c5" 
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/391.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/359.md)

* Arbitrum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/105.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/88.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/99.md)

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/64.md)

* Ink - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/57073/0x44D73D7C4b2f98F426Bf8B5e87628d9eE38ef0Cf/2.md)

* Plasma - [payload Seatbelt report](http://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/2.md)

### Technical Analysis

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.