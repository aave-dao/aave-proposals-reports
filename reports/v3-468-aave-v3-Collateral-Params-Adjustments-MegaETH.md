# Proposal 468. Collateral Parameters Adjustment on MegaETH v3

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=468)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-collateral-parameters-adjustment-on-aave-v3-megaeth-instance/24334)

### Payloads

* MegaETH - [proposal payloads](https://mega.etherscan.io/address/0xdAD7F1b1a16735047BB326C626Baac26C5D910Df)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
This proposal recommends enabling general market (non-eMode) collateral parameters for WETH, BTC.b, and wstETH on the MegaETH Aave deployment. The proposed configurations carry slightly more conservative LTV and liquidation threshold values relative to their respective eMode configurations, reflecting the unconstrained collateral environment of the main pool, and are intended to support cross-margin use cases without compromising the risk isolation benefits of the existing eMode structure.

### Proposal Creation
Transaction: [0x876655ac5cd05c9bbff43f5e40dd2c9cd939e2958e2bc44966d1a854428f3a72](https://etherscan.io/tx/0x876655ac5cd05c9bbff43f5e40dd2c9cd939e2958e2bc44966d1a854428f3a72)
- `proposalId`: 468
- `creator`: 0x66a28531e6f390a8cd44ab0c57a0f1aeb7e673ff
- `accessLevel`: 1
- `ipfsHash`: 0xdf5f9c50eac1197952580733ebd66dfeaf6817377069de8f4db7f78ecfae3426

**`createProposal()` Parameters**
```
{
  "payloads": [ 
    { 
      "chain": "4326", 
      "accessLevel": "1", 
      "payloadsController": "0x80e11cB895a23C901a990239E5534054C66476B5", 
      "payloadId": "2" 
    }, 
  ], 
  "votingPortal": "0x9Ded9406f088C10621BE628EEFf40c1DF396c172", 
  "ipfsHash": "0xdf5f9c50eac1197952580733ebd66dfeaf6817377069de8f4db7f78ecfae3426" 
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/468.md)

**Payload Reports**

* MegaETH - [payload Seatbelt report](https://github.com/aave-dao/seatbelt-gov-v3/blob/main/reports/payloads/4326/0x80e11cB895a23C901a990239E5534054C66476B5/2_forge.md)

### Technical Analysis

We have verified the update to the relevant E-Mode parameters.

We have validated the collateral updates for the relevant assets with the correct risk parameters.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.