# Proposal 437. Onboard syrupUSDC on Base

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=437)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-onboard-syrupusdc-to-aave-v3-base-instance/23234)

### Payloads

* Base - [proposal payloads](https://basescan.org/address/0x5f7d4FE424F1b1a3bF4FeBd624A4b72D965B5dC1)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates
* :gem: :new: Listing new assets


### Context

This AIP proposes to onboard syrupUSDC to Aave V3 Base Instance.

### Proposal Creation
Transaction: [0xc95b1f9301766e5bb9d107b3e325f7f62b1e4021fbdbee925ad27cf265dfa05d](https://etherscan.io/tx/0xc95b1f9301766e5bb9d107b3e325f7f62b1e4021fbdbee925ad27cf265dfa05d)
- `proposalId`: 437
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x40b5da4af3c5e5d8048049bcb42d242a6dc5a6c89db2e351c4aa92108b753fe1

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 95,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x40b5da4af3c5e5d8048049bcb42d242a6dc5a6c89db2e351c4aa92108b753fe1",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/437.md)

**Payload Reports**

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/95.md)


### Technical Analysis

We have checked the alignment of new listing risk parameters between IPFS and the payload.
We have checked the E-Mode risk parameters.
We have verified the `syrupUSDC` address and the `syrupUSDC_LM_ADMIN` address.
We have checked the supply amount, taking decimal precision into account.
We have reviewed the payload logic and validated its execution using the Seatbelt report.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
