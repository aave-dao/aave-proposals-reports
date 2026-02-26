# Proposal 451. Focussing the Aave V3 Multichain Strategy - Phase 1

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=451)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-focussing-the-aave-v3-multichain-strategy-phase-1/23954)

### Payloads

* Metis - [proposal payloads](https://explorer.metis.io/address/0x44ed28fF572264bDd23dB841A72Ce49a8Bc927D3)

* zkSync - [proposal payloads](https://explorer.zksync.io/address/0x85C84A88B18d469C98d6d86E371a2589Ee8bD6E9)

* Soneium - [proposal payloads](https://soneium.blockscout.com/address/0xAe779D9e1d67E4ef1793fAac2Dd03aA9D6CCB9e8)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates


### Context
The proposal plans to provide and execute a multichain strategy for Aave V3 that will freeze the following networks, as a start:

1. zkSync
2. Metis
3. Soneium

This proposal sets to reduce operational overhead and governance burden by addressing instances that are clearly non viable today.

### Proposal Creation
Transaction: [0x0c98e2d576d8c8719f90d3917d005676c338154fafa17ac2613b8ec642e77e7d](https://etherscan.io/tx/0x0c98e2d576d8c8719f90d3917d005676c338154fafa17ac2613b8ec642e77e7d)
- `proposalId`: 451
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x2d69ae54501fa8220cbf922731c65b48dc17f5f80e78ffd1e69003d5aed43aa8

**`createProposal()` Parameters**
```
{
  "payloads": [ 
    { 
      "chain": "1088", 
      "accessLevel": "1", 
      "payloadsController": "0x2233F8A66A728FBa6E1dC95570B25360D07D5524", 
      "payloadId": "47" 
    }, 
    { 
      "chain": "324", 
      "accessLevel": "1", 
      "payloadsController": "0x2E79349c3F5e4751E87b966812C9E65E805996F1", 
      "payloadId": "36" 
    }, 
    { 
      "chain": "1868", 
      "accessLevel": "1", 
      "payloadsController": "0x44D73D7C4b2f98F426Bf8B5e87628d9eE38ef0Cf", 
      "payloadId": "5" 
    }, 
  ], 
  "votingPortal": "0x9Ded9406f088C10621BE628EEFf40c1DF396c172", 
  "ipfsHash": "0x2d69ae54501fa8220cbf922731c65b48dc17f5f80e78ffd1e69003d5aed43aa8" 
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/451.md)

**Payload Reports**

* Metis - [payload Seatbelt report](https://github.com/aave-dao/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/47.md)

* zkSync - [payload Seatbelt report](https://github.com/aave-dao/seatbelt-gov-v3/blob/main/reports/payloads/324/0x2E79349c3F5e4751E87b966812C9E65E805996F1/36.md)

* Soneium - [payload Seatbelt report](https://github.com/aave-dao/seatbelt-gov-v3/blob/main/reports/payloads/1868/0x44D73D7C4b2f98F426Bf8B5e87628d9eE38ef0Cf/5.md)


### Technical Analysis

We have verified the payload logic and execution, confirming that the correct assets are being frozen on **Metis** and **Soneium**.

Regarding **zkSync**: the uploaded payload is not the one originally intended. A different [payload](https://github.com/aave-dao/aave-proposals-v3/blob/main/zksync/src/20251023_Multi_DeprecationOfLowDemandVolatileAssetsOnAaveV3Instances/AaveV3ZkSync_DeprecationOfLowDemandVolatileAssetsOnAaveV3Instances_20251023.sol) was accidentally uploaded, however, as this is a **no-op (no-operation) payload**, there is no technical risk. We are ok with proceeding with the execution as [suggested](https://governance.aave.com/t/arfc-focussing-the-aave-v3-multichain-strategy-phase-1/23954/4) by BGD.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.