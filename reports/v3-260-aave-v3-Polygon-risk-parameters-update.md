# Proposal 260. Adjust Aave Polygon V3 Risk Parameters

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=260)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-adjust-risk-parameters-for-aave-v2-and-v3-on-polygon/20211/60)

### Payloads

* Polygon - [proposal payloads](https://polygonscan.com/address/0xF2D238D3B62F597d8c251832f6Ed16d11663e91F)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates

### Context
This proposal addendum seeks governance approval for adjustment of the AIP-254 to reintroduce LTV for non-bridged stablecoins (USDC,USDT) in Aave Polygon V3.

### Proposal Creation
Transaction: [0x456336cb08f93d8504cbe787d972374aecc7d4ec03303a3bd37bf3211bfda8ac](https://etherscan.io/tx/0x456336cb08f93d8504cbe787d972374aecc7d4ec03303a3bd37bf3211bfda8ac)
- `proposalId`: 260
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x3b936dd6cf7fc54c4a31240ae34a4b6e2a6cf5d540372a76dcf33b28a2b1fb9c

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 102,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0x3b936dd6cf7fc54c4a31240ae34a4b6e2a6cf5d540372a76dcf33b28a2b1fb9c",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/260.md)

**Payload Reports**

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/102.md)


### Technical Analysis
We have verified that the correct tokens ltv was adjusted to 70%, the emode was configured as specified in the forum and ipfs. Additionally that all stablecoins assets were configured to non borrowable in the emode.
The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.