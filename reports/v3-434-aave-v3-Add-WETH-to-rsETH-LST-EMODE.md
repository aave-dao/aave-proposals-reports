# Proposal 434. Add WETH to the rsETH LST E-Mode on Aave Core Instance 

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=434)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-add-weth-to-the-rseth-lst-e-mode-on-aave-core-instance/23425)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x9675a406f28172c0a285FfA809dc5ad94D7E2E9b)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
This proposal seeks to extend utility for rsETH on the Aave V3 Core market by adding WETH debt to the current rsETH/LST E-Mode category.

### Proposal Creation
Transaction: [0x69af6363ef9deb188b4b2f3c3d7709e6e9d9ef86d0a50b36dd0e23512715a342](https://etherscan.io/tx/0x69af6363ef9deb188b4b2f3c3d7709e6e9d9ef86d0a50b36dd0e23512715a342)
- `proposalId`: 434
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x94ab00247cd1ae13dc3c012532f60e3401ea02d57f450b2ba420456b79a411e7

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 394,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x94ab00247cd1ae13dc3c012532f60e3401ea02d57f450b2ba420456b79a411e7",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/434.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/394.md)


### Technical Analysis

We have verified that the E-Mode risk parameters are consistent across the form, IPFS, and the payload.
We reviewed the payload logic and validated it using the Seatbelt execution simulation.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.