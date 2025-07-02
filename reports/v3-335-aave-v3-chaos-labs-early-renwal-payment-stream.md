# Proposal 335. Chaos Labs x Aave DAO — Early Renewal Proposal

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=335)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/chaos-labs-x-aave-dao-early-renewal-proposal/22346)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x1Af1C5F93C17eB0D4e486B5A86b54CAe335cB656)



## Certora Analysis

### Proposal Types

* :bank: Payment stream

### Context
Chaos Labs proposes a 12-month early renewal of our risk management partnership with the Aave DAO, starting July 13, 2025. This renewal will be a new and separate engagement stream, operating in parallel with the current engagement, which remains active through November 12, 2025. The early renewal will not affect the existing engagement and will continue independently through July 12, 2026.

### Proposal Creation
Transaction: [0x672c51253c58319e3ff504912ae344465070c6c73d19f7aa63da28c06b75448d](https://etherscan.io/tx/0x672c51253c58319e3ff504912ae344465070c6c73d19f7aa63da28c06b75448d)
- `proposalId`: 335
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xc39dbb2f31171d7ac1b41f6ad80d6f1c4c44f4da5641d987a42fc07f85dc46bf

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 311,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xc39dbb2f31171d7ac1b41f6ad80d6f1c4c44f4da5641d987a42fc07f85dc46bf",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/335.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/311.md)


### Technical Analysis
We have checked the amounts and the duration are correct.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.