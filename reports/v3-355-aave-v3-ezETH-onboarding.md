# Proposal 355. Add ezETH to Aave v3 Core Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=355)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-add-ezeth-to-aave-v3-core-instance/22732)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x02209E4103CcDB63f3f6fF4B69750808a96E039C)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context
This publication proposes onboarding ezETH as collateral to the Aave V3 Core Instance.


### Proposal Creation
Transaction: [0x7a3649ae39fdccc3000f6fee4a9191ec9c03ecf41f00a4e0d4111749a977195d](https://etherscan.io/tx/0x7a3649ae39fdccc3000f6fee4a9191ec9c03ecf41f00a4e0d4111749a977195d)
- `proposalId`: 355
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x1bd67723b9c2e9025c29f767a7296bdcde1c5af42d48bdfb495ea4d13a881d12

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 329,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x1bd67723b9c2e9025c29f767a7296bdcde1c5af42d48bdfb495ea4d13a881d12",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/355.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/329.md)


### Technical Analysis
We have verified the risk params match the IPFS and forum. We have validated the supply of the seed amount to the pool. We have checked the correctness of the price feed.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.