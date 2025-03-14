# Proposal 266. Collateralize AUSD on V3 Avalanche

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=266)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-chaos-labs-risk-parameters-update-ausd-on-v3-avalanche/21201)

### Payloads

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xb894ca17da54242094f523E4Cd6357C2807e509c)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
Making AUSD into a collateral asset on Aave V3’s Avalanche Deployment.

### Proposal Creation
Transaction: [0x70978616d6b19195c14ce92a157b96d764ff737e42824b6874e22a27f4bf3b76](https://etherscan.io/tx/0x70978616d6b19195c14ce92a157b96d764ff737e42824b6874e22a27f4bf3b76)
- `proposalId`: 266
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xa7cdf42a355a552ebb1e0a7fc43191b85d87c14faff922448d9ad364a78bb328

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 70,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0xa7cdf42a355a552ebb1e0a7fc43191b85d87c14faff922448d9ad364a78bb328",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/266.md)

**Payload Reports**

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/70.md)


### Technical Analysis
We have verified that the intended asset with intended parameters changed correctly. 

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.