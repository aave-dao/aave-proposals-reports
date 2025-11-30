# Proposal 414. Onboard rsETH to Aave V3 Avalanche Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=414)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-onboard-rseth-to-aave-v3-avalanche-instance/23313)

### Payloads

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x20f2b49C3d0022BE1e19EC3430d2146A0009B1DF)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets

### Context
This proposal seeks to onboard rsETH to the Aave V3 deployment on the Avalanche network.

As the onboarding of rsETH has already been approved and executed on the Ethereum, Arbitrum, and Base Aave V3 instances, this proposal follows the Direct-to-AIP path to extend rsETH support to the Avalanche instance without repeating the full ARFC process.

### Proposal Creation
Transaction: [0x8aa7967c748fddc95ffc6d55d205f550853e7828c6fcf091866311251372c9b4](https://etherscan.io/tx/0x8aa7967c748fddc95ffc6d55d205f550853e7828c6fcf091866311251372c9b4)
- `proposalId`: 414
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xbf156d74503ef58e0625124f71e4e5584b30e823996b82e60724656e35be9902

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 101,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xbf156d74503ef58e0625124f71e4e5584b30e823996b82e60724656e35be9902",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/414.md)

**Payload Reports**

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/101.md)


### Technical Analysis
The proposal is consistent with the description on both Snapshot and the governance forum.
We have validated consistency between the risk params.
We have verified token, LM_ADMIN addresses and seed amount with respect to decimal precision.
We have verified E-Mode creation and its params.
The payload logic, contract structure, configuration fields, and imports were checked against Aave V3 standards and static analysis plus execution simulation using Seatbelt confirmed correct behavior and no unexpected state changes.
### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.