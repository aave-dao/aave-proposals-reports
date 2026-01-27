# Proposal 440. Gho Mantle Activation

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=440)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-deploy-aave-v3-on-mantle/20542/10)

### Payloads

* Mantle - [proposal payloads](https://mantlescan.xyz/address/0xe212d6ce6CFc8B6A2FC784242f98bEBacb01c130)

* Ethereum - [proposal payloads](https://etherscan.io/address/0x49E61c53cB201D4376064ED5Cd5f4bD80cdBEC38)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x33A57AB7DD14C75de323130755641c1017510b2c)

* Base - [proposal payloads](https://basescan.org/address/0x0F0dE697c66B6A9A6B902eD60f8141560db62850)

* Avalanche - [proposal payloads](https://snowscan.xyz/address/0x01A5B6fc904899c145F72A183970F6C03bCBC3eB)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0xf6B2Ab7fB18D953acEDAee59D70fB3EEeEEAf356)

* Ink - [proposal payloads](https://explorer.inkonchain.com/address/0xaEbc1055662Ef29C2c5ddf922f0C95DbC4D87871)

* Plasma - [proposal payloads](https://plasmascan.to/address/0xCfACb53E12D9817865ed5Ea4cD2Adab121875E90)





## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates


### Context
{**TODO: Write context.**}

### Proposal Creation
Transaction: [0x74ba88372b8fac5e932722d234512744a56d4bd769b37626ab69d05f241f924a](https://etherscan.io/tx/0x74ba88372b8fac5e932722d234512744a56d4bd769b37626ab69d05f241f924a)
- `proposalId`: 440
- `creator`: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xa7fa3d6deffa0935b423da850dae3a435ebeea70c2098311d0d750bb7df24036

**`createProposal()` Parameters**
```
{
  "payloads": [ 
    { 
      "chain": "5000", 
      "accessLevel": "1", 
      "payloadsController": "0xF089f77173A3009A98c45f49D547BF714A7B1e01", 
      "payloadId": "0" 
    }, 
    { 
      "chain": "1", 
      "accessLevel": "1", 
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5", 
      "payloadId": "397" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "110" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "96" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "106" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "70" 
    }, 
    { 
      "chain": "57073", 
      "accessLevel": "1", 
      "payloadsController": "0x44D73D7C4b2f98F426Bf8B5e87628d9eE38ef0Cf", 
      "payloadId": "3" 
    }, 
    { 
      "chain": "9745", 
      "accessLevel": "1", 
      "payloadsController": "0xe76EB348E65eF163d85ce282125FF5a7F5712A1d", 
      "payloadId": "16" 
    }, 
  ], 
  "votingPortal": "0x9Ded9406f088C10621BE628EEFf40c1DF396c172", 
  "ipfsHash": "0xa7fa3d6deffa0935b423da850dae3a435ebeea70c2098311d0d750bb7df24036" 
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report]()

**Payload Reports**



* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/397.md)

* Arbitrum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/110.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/96.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/106.md)

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/70.md)

* Ink - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/57073/0x44D73D7C4b2f98F426Bf8B5e87628d9eE38ef0Cf/3.md)

* Plasma - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/16.md)

### Technical Analysis

We have verified that the addresses specified in the IPFS payload match the Mantle payload addresses.

We have verified that all the lanes are set up correctly, with a rate limit of 1.5M GHO capacity and 300 GHO per second rate. 

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.