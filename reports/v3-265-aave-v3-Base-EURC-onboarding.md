# Proposal 265. Add EURC to BASE Aave V3

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=265)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-add-eurc-to-base-aave-v3/20680)

### Payloads

* Base - [proposal payloads](https://basescan.org/address/0xd94E351C288d46192bA3d8f457A2dE4c692F9Bc8)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context
The current ARFC proposes to add EURC on Base V3. EURC is Circle’s EUR-backed stablecoin, enhancing liquidity and expanding the platform’s appeal to European users.

### Proposal Creation
Transaction: [0xfc9992cb4aad80807f120a37a803941df7cac5b6dbfa35ec9354f9731c791596](https://etherscan.io/tx/0xfc9992cb4aad80807f120a37a803941df7cac5b6dbfa35ec9354f9731c791596)
- `proposalId`: 265
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x42c291379ab2a90483a8ccd4e76461521f0a8178159bc3de2b960de724e579e6

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 59,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0x42c291379ab2a90483a8ccd4e76461521f0a8178159bc3de2b960de724e579e6",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/265.md)

**Payload Reports**

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/59.md)


### Technical Analysis
We have verified that the specified parameters match the specification, we have verified the supply of seed amount and use of a correct price feed.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.