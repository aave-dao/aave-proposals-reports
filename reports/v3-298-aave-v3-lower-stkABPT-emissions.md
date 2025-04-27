# Proposal 298. Lower stkABPT Emissions

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=298)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-stkabpt-emissions-update/21683)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xd161bdA38b7499E2D44d9C37675Ff47Bc9A3F256)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates

### Context
This publication proposes reducing AAVE emissions to the stkABPT Safety Module category.

### Proposal Creation
Transaction: [0x9888e683241899729fc6fb3446046cbc134bc6b683a9a92e109f520aedd9fde5](https://etherscan.io/tx/0x9888e683241899729fc6fb3446046cbc134bc6b683a9a92e109f520aedd9fde5)
- `proposalId`: 298
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x806c9d92b382f5668422f150a8d11c8347d3e0e6419b7e73185784f75d3e7d55

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 278,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x806c9d92b382f5668422f150a8d11c8347d3e0e6419b7e73185784f75d3e7d55",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/298.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/278.md)


### Technical Analysis
## Safety Module Update Verification

We’ve confirmed that the Safety Module proxy now points to the new **StakeToken** implementation, and that both the emission index and the per-second emission rate were updated to exactly **2 777 777 777 777 777 wei/s** (≈ 240 AAVE per day).

* The two ERC-20 approvals (first zero, then new allowance + leftover) align with the reserve-allowance logic in the proposal.  
* The governance executor’s **ExecutedAction** event, followed by the final **PayloadExecuted** event, proves the payload ran to completion.  
* All expected events are present; none are missing.  
* The tiny integer-division rounding shortfall (~ 6 × 10⁴ wei/day) is functionally negligible.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.