# Proposal 341. amend PT-sUSDe september stablecoin emode

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=341)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-adjustment-of-pt-susde-september-e-mode-and-usdtb-ir-curve/22615)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xd4b898881803B0ca6b798e62DA096FA831fC7418)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
This proposal recommends enabling USDtb as a borrowable asset within the e-mode configuration for USDe PTs and adding sUSDe and PT-sUSDE-31JUL2025 as a collateral asset to the stablecoin e-mode configuration of PT-sUSDe-25SEP2025.

### Proposal Creation
Transaction: [0x8045e018d255bf7fe2a54a3c7583e105fb4300fbb5747498f427d0b0b9c6de2d](https://etherscan.io/tx/0x8045e018d255bf7fe2a54a3c7583e105fb4300fbb5747498f427d0b0b9c6de2d)
- `proposalId`: 341
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x7a5b98aa1030964b1ba754fc35d2e3d3e17549c97ee82977d6a5fc56d8fd198b

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 318,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x7a5b98aa1030964b1ba754fc35d2e3d3e17549c97ee82977d6a5fc56d8fd198b",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/341.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/318.md)


### Technical Analysis
We have verified that the correct assets have been added to the e-mode, with respect to their collateral and borrow enablement statuses.
The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.