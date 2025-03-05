# Proposal 263. wrsETH Base Onboarding

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=263)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-onboard-rseth-to-arbitrum-and-base-v3-instances/20741)

### Payloads

* Base - [proposal payloads](https://basescan.org/address/0xCAD96AF06E01817b62A46B6343691a98e114Fa43)


## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context
This is an AIP to onboard rsETH to the Aave V3 Base Instance allowing Aave users to supply wrsETH as collateral. This proposal will be under Direct to AIP, as rsETH is already listed on other Aave instances.

### Proposal Creation
Transaction: [0x51062eb3e973342787d3669e8f8b60d475c0d67155b0843143b769245521bca6](https://etherscan.io/tx/0x51062eb3e973342787d3669e8f8b60d475c0d67155b0843143b769245521bca6)
- `proposalId`: 263
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x6fba0be9251581b6628c378a8cfef6bba51a0a902528bfc4b0eff92ed14635b8

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 57,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0x6fba0be9251581b6628c378a8cfef6bba51a0a902528bfc4b0eff92ed14635b8",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/263.md)

**Payload Reports**

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/57.md)


### Technical Analysis
We have verified that the risk parameters have configure properly to the intended values in the correct decimals representation. We have verified the price feed oracle correctness (chain link correct ratio wrsETH/ eth , eth/usd).

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.