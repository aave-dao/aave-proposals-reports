# Proposal 460. Aave V3.6 XLayer Activation

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=460)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-deploy-aave-v3-on-x-layer/23175/18)

### Payloads

* XLayer - [proposal payloads](https://www.oklink.com/xlayer/address/0x7A979E542fdbE380A4c5398aA50dEA6F5C94Aefa)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
This proposal reduces Safety Module emissions and adjusts parameters for stkAAVE and stkAAVE/wstETH BPTv2, saving a combined 29,200 AAVE/year (~0.18% of total supply, ~$3.6M) while transitioning stkAAVE/wstETH BPTv2 toward sunset in favour of Protocol-Owned Liquidity.

### Proposal Creation
Transaction: [0x3d63f220cb9c9ebe496c32d4d5ebb6d012db229a89e26e094a5369a19f8ec2bf](https://etherscan.io/tx/0x3d63f220cb9c9ebe496c32d4d5ebb6d012db229a89e26e094a5369a19f8ec2bf)
- `proposalId`: 460
- `creator`: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- `accessLevel`: 1
- `ipfsHash`: 0xd5704219e5f118e3939ac3d2624ecfd8ff03a5857eeecc27c6fbdf9a8491bbeb

**`createProposal()` Parameters**
```
{
  "payloads": [ 
    { 
      "chain": "196", 
      "accessLevel": "1", 
      "payloadsController": "0x80e11cB895a23C901a990239E5534054C66476B5", 
      "payloadId": "1" 
    }, 
  ], 
  "votingPortal": "0x9Ded9406f088C10621BE628EEFf40c1DF396c172", 
  "ipfsHash": "0xd5704219e5f118e3939ac3d2624ecfd8ff03a5857eeecc27c6fbdf9a8491bbeb" 
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/460.md)

**Payload Reports**

* XLayer - [payload Seatbelt report](https://github.com/aave-dao/seatbelt-gov-v3/blob/main/reports/payloads/196/0x80e11cB895a23C901a990239E5534054C66476B5/1.md)


### Technical Analysis
We verified seed amounts with respect to token decimal precision.

We verified token addresses, Chainlink price feed addresses (including the custom adapters for stablecoins and correlated assets), and all risk parameters.

We reviewed all E-Mode categories and their configurations.

We verified all listing parameters for the newly added assets.

We validated the payload logic and confirmed execution via Seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.