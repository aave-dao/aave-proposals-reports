# Proposal 257. Aave V3.3 Sonic Activation

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=257)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-deploy-aave-v3-on-sonic/20543/26)

### Payloads

* Sonic - [proposal payloads](https://sonicscan.org//address/0x23BEEA83a3463242209E985D465cD85e2A75343A)



## Certora Analysis

### Proposal Types
* :handshake: Permission granting and revoking
* :gem: :new: Listing new assets

### Context
Following the DAO's approval to activate Aave on Sonic, this proposal grant essential roles maintanance roles and lists the first assets on the instance.

### Proposal Creation
Transaction: [0xed5714aff09f0c208711c1bce637a2cbcb145ba7636c8dabfd4b93464f799851](https://etherscan.io/tx/0xed5714aff09f0c208711c1bce637a2cbcb145ba7636c8dabfd4b93464f799851)
- `proposalId`: 257
- `creator`: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- `accessLevel`: 1
- `ipfsHash`: 0xf6582bfdcba3fe0dea34d09d59afa65489e2e683345e0d3812c0975ebfc3d75a

**`createProposal()` Parameters**
```
{
  "payloads": [ 
    { 
      "chain": "146", 
      "accessLevel": "1", 
      "payloadsController": "0x0846C28Dd54DEA4Fd7Fb31bcc5EB81673D68c695", 
      "payloadId": "0" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xf6582bfdcba3fe0dea34d09d59afa65489e2e683345e0d3812c0975ebfc3d75a" 
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/257.md)

**Payload Reports**

* Sonic - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/146/0x0846C28Dd54DEA4Fd7Fb31bcc5EB81673D68c695/0.md)


### Technical Analysis
We verified that the proposal sets the protocol guardian with a pool admin role and the risk steward with a pool risk admin role. In addition, the proposal lists 3 new asset to the Sonic network - wS, wETH, USDC - with the parameters specified in the proposal description.

Moreover, for each underlying and aToken of the newly listed asset, the proposal sets the ACI multisig as the emission manager.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.