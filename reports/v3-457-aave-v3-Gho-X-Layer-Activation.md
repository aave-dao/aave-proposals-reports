# Proposal 440. Gho X-Layer Activation

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=457)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-launch-gho-on-x-layer-set-aci-as-emissions-manager-for-rewards/23178)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xF278dE48F4Fc9C1fB43bD33387301Ccbf774Dc5A)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x46466E924b4E37602bA2F0386498d39aae865615)

* Base - [proposal payloads](https://basescan.org/address/0xb3A9765D7BC06F1C30CCBD8D7241CdCed80988CB)

* Avalanche - [proposal payloads](https://snowscan.xyz/address/0xc2c7c62e6Ef7Df4fCe0c8E2f3Fec4f3fb14eD995)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x77Be64545b1FF0B464A78F213e8E557D0ee124d5)

* Ink - [proposal payloads](https://explorer.inkonchain.com/address/0xDB2C74653b9A9b309d6Caff05Ed9Cc33d5F9e50F)

* Plasma - [proposal payloads](https://plasmascan.to/address/0x6F0BaBDA7B1Eda822a425Be2963af8E9b912AFc9)

* Mantle - [proposal payloads](https://mantlescan.xyz/address/0x415a0D9A165EFE8530A8094b7e05788e5909DAf1)

* X-Layer - [proposal payloads](https://www.oklink.com/x-layer/address/0x6F0BaBDA7B1Eda822a425Be2963af8E9b912AFc9)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates


### Context
This AIP proposes activating CCIP Lanes for GHO on the X-Layer blockchain.


### Proposal Creation
Transaction: [0xff0deb9d0768a61e80994542543c7c301fad46c0bff0cc2fa9eb801e36af8c08](https://etherscan.io/tx/0xff0deb9d0768a61e80994542543c7c301fad46c0bff0cc2fa9eb801e36af8c08)
- proposalId: 457
 - creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
 - accessLevel: 1
 - ipfsHash: 0x21f179b3f9bca279e03a7231941ba908b9ab8617391ce0956593a7ac74f17dba

**`createProposal()` Parameters**
```
{
  "payloads": [ 
    { 
      "chain": "1", 
      "accessLevel": "1", 
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5", 
      "payloadId": "412" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "110" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "114" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "101" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "72" 
    }, 
    { 
      "chain": "57073", 
      "accessLevel": "1", 
      "payloadsController": "0x44D73D7C4b2f98F426Bf8B5e87628d9eE38ef0Cf", 
      "payloadId": "4" 
    }, 
    { 
      "chain": "5000", 
      "accessLevel": "1", 
      "payloadsController": "0xF089f77173A3009A98c45f49D547BF714A7B1e01", 
      "payloadId": "3" 
    }, 
    { 
      "chain": "9745", 
      "accessLevel": "1", 
      "payloadsController": "0xe76EB348E65eF163d85ce282125FF5a7F5712A1d", 
      "payloadId": "20" 
    }, 
    { 
      "chain": "196", 
      "accessLevel": "1", 
      "payloadsController": "0x80e11cB895a23C901a990239E5534054C66476B5", 
      "payloadId": "0" 
    }, 
  ], 
  "votingPortal": "0x9Ded9406f088C10621BE628EEFf40c1DF396c172", 
  "ipfsHash": "0x21f179b3f9bca279e03a7231941ba908b9ab8617391ce0956593a7ac74f17dba" 
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report]()

**Payload Reports**



* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/412.md)

* Arbitrum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/114.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/101.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/110.md)

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/72.md)

* Ink - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/57073/0x44D73D7C4b2f98F426Bf8B5e87628d9eE38ef0Cf/4.md)

* Plasma - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/16.md)

* Mantle - [payload Seatbelt report](https://github.com/aave-dao/seatbelt-gov-v3/blob/main/reports/payloads/5000/0xF089f77173A3009A98c45f49D547BF714A7B1e01/3.md)

* X-Layer - [payload Seatbelt report](https://github.com/aave-dao/seatbelt-gov-v3/blob/main/reports/payloads/196/0x80e11cB895a23C901a990239E5534054C66476B5/0.md)

### Technical Analysis

We have verified that the addresses specified in the IPFS payload match the Mantle payload addresses.

We have verified that all the lanes are set up correctly, with a rate limit of 1.5M GHO capacity and 300 GHO per second rate. 

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.