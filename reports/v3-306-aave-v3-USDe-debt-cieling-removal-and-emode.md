# Proposal 306.  Remove USDe Debt Ceiling and Introduce USDe Stablecoins E-mode

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=306)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-remove-usde-debt-ceiling-and-introduce-usde-stablecoins-e-mode/21876)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xea0420Bd3C138586B7CB299Bfa7AE4C0a85c582B)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
Given the significant demand for USDe and its safe usage profile on Aave V3’s Ethereum Core deployment, Chaos Labs recommends removing the asset’s debt ceiling and introducing a new E-Mode configuration tailored to its current primary use case.

### Proposal Creation
Transaction: [0xd830d6553b3e5f1f61694df75b5c784744ec39c167ec479fdecb73f44b524e56](https://etherscan.io/tx/0xd830d6553b3e5f1f61694df75b5c784744ec39c167ec479fdecb73f44b524e56)
- `proposalId`: 306
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x806915ad5b7747849fcfcca9d14f71c55d9bb33280e8a6a73f8082503af2cc06

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 285,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x806915ad5b7747849fcfcca9d14f71c55d9bb33280e8a6a73f8082503af2cc06",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/306.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/285.md)


### Technical Analysis
We have validated the debt ceiling is initialized and the emode was configured correctly to a new ID.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.