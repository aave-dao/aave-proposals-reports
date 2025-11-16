# Proposal 393. Onboard wrsETH to Aave v3 Plasma Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=393)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-onboard-wrseth-to-aave-v3-plasma-instance/23183)

### Payloads

* Plasma - [proposal payloads](https://plasmascan.to/address/0x5412Bf87245e0a8E1d06904B5d909Ff71baAF799)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context
This publication proposes adding wstETH and wrsETH as collateral to the Aave v3 instance on the Plasma network using the Direct-to-AIP process.



### Proposal Creation
Transaction: [0xd2fd7d8f1356d1a7c1d4944679d1023d925e3bca6879bc31264d8791130f4f09](https://etherscan.io/tx/0xd2fd7d8f1356d1a7c1d4944679d1023d925e3bca6879bc31264d8791130f4f09)
- `proposalId`: 393
- `creator`: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xc20b7c25c84c6dd8c656c9834863ef321f9c4240e76f58b6a798c363f9c53584

**`createProposal()` Parameters**
```
{
  "payloads": [ 
    { 
      "chain": "9745", 
      "accessLevel": "1", 
      "payloadsController": "0xe76EB348E65eF163d85ce282125FF5a7F5712A1d", 
      "payloadId": "4" 
    }, 
  ], 
  "votingPortal": "0x9Ded9406f088C10621BE628EEFf40c1DF396c172", 
  "ipfsHash": "0xc20b7c25c84c6dd8c656c9834863ef321f9c4240e76f58b6a798c363f9c53584" 
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/4.md)

**Payload Reports**

* Plasma - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/4.md)


### Technical Analysis

We have validated and compared the risk parameters with respect to decimal precision. We have confirmed the validity of the `wrsETH` and `wstETH` address tokens and price feeds. The seed supply was correctly implemented as well. We have found typo in the ipfs and contacted ACI for clarification.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.