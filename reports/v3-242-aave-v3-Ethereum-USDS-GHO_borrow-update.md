# Proposal 242. Update USDS & GHO Borrow Rate

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=242)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-update-usds-gho-borrow-rate/20892)

### Payloads

* Ethereum Core - [proposal payloads](https://etherscan.io/address/0x0c067D28f4ED6d921975535fD16742D2C257897F)

* Ethereum Prime - [proposal payloads](https://etherscan.io/address/0x8cA0Fa6D172bF5f56bdc1C5B8d976eAF1aCdA31B)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
The Sky Savings Rate (SSR) is expected to be lowered from 12.50% to 9.50% on February 10th. This publication proposes updating the USDS Borrow Rate and also, reducing the GHO Borrow Rate on the Prime instance. This update will be conducted via a Direct-to-AIP process.


### Proposal Creation
Transaction: [0xfe68de0be1c7c74b739fb74bd8a53a8d80a3c9ce193eb0ab480d64fe8bed2f44](https://etherscan.io/tx/0xfe68de0be1c7c74b739fb74bd8a53a8d80a3c9ce193eb0ab480d64fe8bed2f44)
- `proposalId`: 242
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x6b4cfbdb8b59afd1d576bcf041c38afc2c470371f03aed459ba0a728244702ac

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 242,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0x6b4cfbdb8b59afd1d576bcf041c38afc2c470371f03aed459ba0a728244702ac",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/242.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/242.md)


### Technical Analysis
Upon reviewing the borrow rate parameters we have found a discrepancy between the implementation and the forum in which the `baseVariableBorrowRate` for GHO was configured to 6% instead of 5.75%. The issue was addressed by ACI with the use of steward after the payload is executed.

Other parameters were compatible with the specification.


The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.