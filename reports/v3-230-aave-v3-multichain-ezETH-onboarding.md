# Proposal 230. Onboard ezETH to Arbitrum and Base Instances

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=230)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-onboard-ezeth-to-arbitrum-and-base-instances/19622)

### Payloads

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0x0EFc2A29c1f203a29DfDc3B8a723DD67d1d9a42d)

* Base - [proposal payloads](https://basescan.org/address/0xcAb93fDD35d1F0A8dE2627eD99188953Bcd6933B)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context
This is an AIP for adding borrow/lend support for Renzo Protocol and its Liquid Restaking Token (LRT) ezETH on AAVE V3 Base and Arbitrum.

### Proposal Creation
Transaction: [0x9948f6f57ff804c0633ab0654cfb226c96b5af21be026fe87f32d594a431baa7](https://etherscan.io/tx/0x9948f6f57ff804c0633ab0654cfb226c96b5af21be026fe87f32d594a431baa7)
- `proposalId`: 230
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x5fcc204c8e20a3eccd431a9d84f28910d233c1d65cc2e1d88b062e9daaf28522

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 67,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 49,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0x5fcc204c8e20a3eccd431a9d84f28910d233c1d65cc2e1d88b062e9daaf28522",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/230.md)

**Payload Reports**

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/67.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/49.md)


### Technical Analysis
We performed a comprehensive technical analysis by comparing the parameters available on IPFS and verifying that the correct configuration is reflected in the implementation. Our review included checking the price feed oracles and confirming that the first deposit parameters are set correctly. All verified settings match the documented expectations, ensuring consistency and correct behavior in the deployed environment.


The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.