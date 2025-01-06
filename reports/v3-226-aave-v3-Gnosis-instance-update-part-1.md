# Proposal 226. Gnosis Instance Updates Part 1

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=226)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-aave-v3-gnosis-instance-updates/20334)

### Payloads

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x58B1824B9b1c417551E1c5080645FedcBc602574)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates

### Context
This AIP proposes several updates to the Aave v3 Gnosis instance to improve capital efficiency and add new use cases on the network. The key changes include removing GNO from isolation mode, adjusting the reserve factor for EURe, and creating a new relevant E-mode.

### Proposal Creation
Transaction: [0xb9ab8a65a16d9271bd556c68ee6afae98873e055bf5e446a3c56eeee2edaa564](https://etherscan.io/tx/0xb9ab8a65a16d9271bd556c68ee6afae98873e055bf5e446a3c56eeee2edaa564)
- `proposalId`: 226
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xe85e3756a4d99d94cd69529df732df35022726eb9cadfdb3968bf25813648b51

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "100",
            accessLevel: 1,
            payloadsController: "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
            payloadId: 40,
        },
    ],
    votingPortal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfsHash: "0xe85e3756a4d99d94cd69529df732df35022726eb9cadfdb3968bf25813648b51",
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/226.md)

**Payload Reports**

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/40.md)


### Technical Analysis
We have verified that the assets configured correctly and the new emode created and configured correctly.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.