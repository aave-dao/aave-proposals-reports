# Proposal 383. Aave v2 Deprecation - Update

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=383)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-aave-v2-deprecation-update/23008/2)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xC5c4A55d63959720E0DAFA4c18EC8E57Ba8E83CC)

* Polygon - [proposal payloads](https://polygonscan.com/address/0xA0280DBB0e471233bcbac86F1DC56612AA794aF9)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x10ac4E8Fa8bA71f7dC2176763D0EDe7f640f9652)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates

### Context
This proposal presents the next round of parameter updates to be implemented as we work towards deprecating v2 instances of Aave Protocol across Polygon, Ethereum and Avalanche.

### Proposal Creation
Transaction: [0x28223768120cf2fbb798aced463548265eae61c09411e347b465b62307bbb560](https://etherscan.io/tx/0x28223768120cf2fbb798aced463548265eae61c09411e347b465b62307bbb560)
- `proposalId`: 383
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xeebe6f3200ce589673f94a5c3ae90186c4bc59e7d7f29a81cb6952149760dd7e

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 351,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 129,
        },
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 97,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xeebe6f3200ce589673f94a5c3ae90186c4bc59e7d7f29a81cb6952149760dd7e",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/383.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/351.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/129.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/97.md)


### Technical Analysis
We have matched the payload to the specified risk parameters change with respect to the decimal precision. We have made sure the correct functions have been used to change every risk parameter.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.