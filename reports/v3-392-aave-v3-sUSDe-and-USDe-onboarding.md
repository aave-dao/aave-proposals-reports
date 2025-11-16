# Proposal 392. Onboard sUSDe and USDe January expiry PT tokens on Aave V3 Plasma Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=392)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-onboard-susde-and-usde-january-expiry-pt-tokens-on-aave-v3-plasma-instance/23196)

### Payloads

* Plasma - [proposal payloads](https://plasmascan.to/address/0x89C12FD2e7E9D63205Cc1880521eC80E3e7778D7)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context
This AIP proposes to onboard sUSDe and USDe January expiry PT tokens on Aave V3 Plasma Instance. The previous `Ethena` (sUSDe and USDe) PT tokens that were onboarded have brought significant inflows to Aave, given the success of the Plasma instance launch along with the significant USDe and sUSDe liquidity on this instance we believe that onboarding Ethena PT tokens there is a logical next step.

### Proposal Creation
Transaction: [0x145a97798434dfa95ddb93c0367349afac65ef745f1481e1505795711e8eec15](https://etherscan.io/tx/0x145a97798434dfa95ddb93c0367349afac65ef745f1481e1505795711e8eec15)
- `proposalId`: 392
- `creator`: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x14332c8c7c63e94c2b1a67f4cbd3f49dd03a6fecb9b9985ee5dbf1b624d70129

**`createProposal()` Parameters**
```
{
  "payloads": [ 
    { 
      "chain": "9745", 
      "accessLevel": "1", 
      "payloadsController": "0xe76EB348E65eF163d85ce282125FF5a7F5712A1d", 
      "payloadId": "3" 
    }, 
  ], 
  "votingPortal": "0x9Ded9406f088C10621BE628EEFf40c1DF396c172", 
  "ipfsHash": "0x14332c8c7c63e94c2b1a67f4cbd3f49dd03a6fecb9b9985ee5dbf1b624d70129" 
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/3.md)

**Payload Reports**

* Plasma - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/3.md)


### Technical Analysis

We have validated and compared the risk parameters with respect to decimal precision. We have confirmed the validity of the `sUSDe` and `USDe` address tokens and price feeds. The seed supply was correctly implemented as well. 

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.