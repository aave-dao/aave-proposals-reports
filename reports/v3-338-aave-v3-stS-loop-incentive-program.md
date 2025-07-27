# Proposal 338. stS Loop Incentive Program

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=338)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-sts-loop-incentive-program/22368)

### Payloads



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking


### Context
This ARFC proposes the launch of a 3-month stS loop incentive program on Aave. The goal is to deepen stS liquidity on Aave, align incentives with Beets, and ensure Aave remains the exclusive lending market for stS.

### Proposal Creation
Transaction: [0x072f1ad8da3cdb7e306aa95ee74a2d571f5cf852105bf7a0c91337349d86f35c](https://etherscan.io/tx/0x072f1ad8da3cdb7e306aa95ee74a2d571f5cf852105bf7a0c91337349d86f35c)
- `proposalId`: 338
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x5b14be276f0ef509cfb725d201e64d1a8d46c811b23a56e8e19117ba97f4fd27

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "146",
            payloads_controller: "0x0846C28Dd54DEA4Fd7Fb31bcc5EB81673D68c695",
            payload_id: 6,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x5b14be276f0ef509cfb725d201e64d1a8d46c811b23a56e8e19117ba97f4fd27",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/338.md)

**Payload Reports**


### Technical Analysis
We have verified the address and amount are as specified on the IPFS and forum
 
The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.