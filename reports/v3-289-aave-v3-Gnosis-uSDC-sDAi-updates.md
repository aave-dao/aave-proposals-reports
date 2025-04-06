# Proposal 289. Enhancements in Aave v3 Gnosis Chain Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=289)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-enhancements-in-aave-v3-gnosis-chain-instance/21214)

### Payloads

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0xc1553D740398f3f1E89d521d37305A8156aF55DA)



## Certora Analysis

### Proposal Types
* :wrench: :bar_chart: Configuration updates

### Context
This publication proposes changes in the Gnosis Chain instance to improve the capital efficiency of USDC.e and sDAI assets by promoting changes on its parametrization.

### Proposal Creation
Transaction: [0x07a9546fdde6c0bf82b543a087f3f932aac7c958004927ca77cf41845b30304d](https://etherscan.io/tx/0x07a9546fdde6c0bf82b543a087f3f932aac7c958004927ca77cf41845b30304d)
- `proposalId`: 289
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x842e291fcdf10a54e43af6d356bf4ed54ef5b33c284f2693f201b6c7875e7633

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "100",
            payloads_controller: "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
            payload_id: 50,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x842e291fcdf10a54e43af6d356bf4ed54ef5b33c284f2693f201b6c7875e7633",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/289.md)

**Payload Reports**

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/50.md)


### Technical Analysis
We have confirmed the correct asset were modified. The risk parameters were changed to the correct values. The new emode was created to the correct id.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.