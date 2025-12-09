# Proposal 418. XAUt Supply Cap and Debt Ceiling Adjustment on Aave V3 Core Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=418)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-xaut-supply-cap-and-debt-ceiling-adjustment-on-aave-v3-core-instance/23466)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x7E386B4a4Fb8695D88bB49bEeed45ECd08C20f88)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
Chaos Labs proposes increasing the XAUt debt ceiling and supply cap following strong utilization and demand. Thanks to strong liquidity, improved market efficiency and safe user behavior, the growth of the asset does not introduce additional risk. Below is our analysis and recommendation.

### Proposal Creation
Transaction: [0xd297aa4293805da8f8dbd6d9f36ace82248dc6b15fede875db31a1922d6c878d](https://etherscan.io/tx/0xd297aa4293805da8f8dbd6d9f36ace82248dc6b15fede875db31a1922d6c878d)
- `proposalId`: 418
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x9a5336582f4cc10f29128ba051dc4e3e5ff9a0d83229c7589fded56ec1488529

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 377,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x9a5336582f4cc10f29128ba051dc4e3e5ff9a0d83229c7589fded56ec1488529",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/418.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/377.md)


### Technical Analysis
We have verified consistency between the forum, IPFS, and the proposal’s payload. We have verified the integrity of the imports. We have checked the payload’s execution logic and validated it via Seatbelt. The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.