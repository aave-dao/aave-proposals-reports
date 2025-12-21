# Proposal 424. Add WETH to the wrsETH wstETH E-Mode on Aave V3 Base Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=424)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-add-weth-to-the-wrseth-wsteth-e-mode-on-aave-v3-base-instance/23431)

### Payloads

* Base - [proposal payloads](https://basescan.org/address/0x8897357a62DAE935D399658d03f21109331F20Cb)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
This proposal seeks to extend utility for wrsETH on the Aave V3 Base market by adding WETH borrowing to the existing wrsETH/wstETH E-Mode category.

### Proposal Creation
Transaction: [0x713c6019740246415da5bdaad3c827f2b39e60d175ee2ab5044b6fc700aedd90](https://etherscan.io/tx/0x713c6019740246415da5bdaad3c827f2b39e60d175ee2ab5044b6fc700aedd90)
- `proposalId`: 424
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x7e39acd608fad0ed3dbdf07691c2e9f629c3f2d19b8730330d23eb8b08cf3453

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 91,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x7e39acd608fad0ed3dbdf07691c2e9f629c3f2d19b8730330d23eb8b08cf3453",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/424.md)

**Payload Reports**

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/91.md)


### Technical Analysis

We have verified the imports.
We have checked alignment between the Forum, IPFS, and the payload.
We have validated the wETH address and confirmed that it is the correct E-Mode.
We have checked the payload’s execution logic and confirmed its execution with Seatbelt.
The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.