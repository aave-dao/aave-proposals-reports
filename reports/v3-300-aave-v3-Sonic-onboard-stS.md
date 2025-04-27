# Proposal 300. Add stS to Aave v3 Sonic Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=300)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-add-sts-to-aave-v3-sonic-instance/21445/5)

### Payloads

* Sonic - [proposal payloads](https://sonicscan.org//address/0x17A0fDDd429C3632EC74E8Bb447328F56c904dca)



## Certora Analysis

### Proposal Types
* :gem: :new: Listing new assets

### Context
The proposal aims to onboard Beets’s stS, to Aave v3 Sonic instance.

### Proposal Creation
Transaction: [0x122f3d4f235e39824ede37b37231f15312a179f60d6c5f9d779661fb74059209](https://etherscan.io/tx/0x122f3d4f235e39824ede37b37231f15312a179f60d6c5f9d779661fb74059209)
- `proposalId`: 300
- `creator`: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x2ca79386fa0a3522378c246e869033e49c153e99b23d4519a3f90e8efef9e191

**`createProposal()` Parameters**
```
{
  "payloads": [ 
    { 
      "chain": "146", 
      "accessLevel": "1", 
      "payloadsController": "0x0846C28Dd54DEA4Fd7Fb31bcc5EB81673D68c695", 
      "payloadId": "3" 
    }, 
  ], 
  "votingPortal": "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6", 
  "ipfsHash": "0x2ca79386fa0a3522378c246e869033e49c153e99b23d4519a3f90e8efef9e191" 
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/300.md)

**Payload Reports**

* Sonic - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/146/0x0846C28Dd54DEA4Fd7Fb31bcc5EB81673D68c695/3.md)


### Technical Analysis
We have verified the risk parameters are as specified in the ipfs. We have verified the price feed has the correct capo and chainlink price feed source.

Moreover, for each underlying and aToken of the newly listed asset, the proposal sets the ACI multisig as the emission manager.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.