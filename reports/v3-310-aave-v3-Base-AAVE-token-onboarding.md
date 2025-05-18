# Proposal 310. Add AAVE token to Aave V3 Base Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=310)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-add-aave-token-to-aave-v3-base-instance/21105)

### Payloads

* Base - [proposal payloads](https://basescan.org/address/0x8B703005e5618B13D9C6397Deea82C18C7b4525c)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets

### Context
This publication presents the community an opportunity to expand AAVE governance token integration on the AAVE platform by adding AAVE collateral option to Base.

AAVE token has wide integrations into all other major AAVE instances including ETH Mainnet, Arbitrum, Optimism, Polygon, and Avalanche. Adding AAVE to the Base instance is the next logical step in AAVE token integration within the AAVE lending platform.

### Proposal Creation
Transaction: [0x1fbfd6ddc789bcb2018ac2da5a9804bb87135cc43083485edafb972325143763](https://etherscan.io/tx/0x1fbfd6ddc789bcb2018ac2da5a9804bb87135cc43083485edafb972325143763)
- `proposalId`: 310
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x7a072a9287642a0b0bd61b39e196534a9c0feaa8382aaeba67ef6bac9e872318

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 68,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x7a072a9287642a0b0bd61b39e196534a9c0feaa8382aaeba67ef6bac9e872318",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/310.md)

**Payload Reports**

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/68.md)


### Technical Analysis
We reviewed each risk parameter in the IPFS spec against the on-chain payload, confirmed that all percentage values (LTV, thresholds, rates, etc.) were correctly scaled in code. We have verified the price feed and checked the seed supply.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.