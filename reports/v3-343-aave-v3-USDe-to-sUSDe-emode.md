# Proposal 343. Add USDe to the sUSDe emode Category

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=343)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-add-usde-to-the-susde-emode-category/22657)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x3DFeAbEd49E218F6EB359e4e78cf02284aBA8dE7)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates



### Context
This proposal aims to add USDe as collateral to the existing sUSDe/Stablecoins emode category to improve capital efficiency and provide a more cohesive borrowing experience for users of Ethena assets on Aave.


### Proposal Creation
Transaction: [0x7861841322dbaf3ae90539c57b12031c9925f77aab160f65f51ccafba60e3cea](https://etherscan.io/tx/0x7861841322dbaf3ae90539c57b12031c9925f77aab160f65f51ccafba60e3cea)
- `proposalId`: 343
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x8e7a70da64e3a8c4f485779aaaa48b9976fff80129aa29815807c8549068354b

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 320,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x8e7a70da64e3a8c4f485779aaaa48b9976fff80129aa29815807c8549068354b",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/343.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/320.md)


### Technical Analysis
We have verified the `USDe` token has been added as collateral to the correct emode.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.