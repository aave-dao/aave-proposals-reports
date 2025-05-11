# Proposal 301. ACI Phase IV – “Road to 80”

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=301)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-aci-phase-iv-road-to-80/21830)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x3Bfc0cAcBD9a98BeF3788Bb803De53346A5489b2)



## Certora Analysis

### Proposal Types

* :bank: Payment stream

### Context
This ARFC proposes renewing and expanding the Aave Chan Initiative’s (ACI) mandate as the Aave DAO’s Growth and Governance Coordination service provider.

### Proposal Creation
Transaction: [0xb8ee7855e9cc7408a2417985be7e54fc6794b09f920021e3a84adf88c7536cc3](https://etherscan.io/tx/0xb8ee7855e9cc7408a2417985be7e54fc6794b09f920021e3a84adf88c7536cc3)
- `proposalId`: 301
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xdd33bc41daa67bd67aacfd29e3907856bda4c131855a5246009b680ade24938a

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 279,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xdd33bc41daa67bd67aacfd29e3907856bda4c131855a5246009b680ade24938a",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/301.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/279.md)


### Technical Analysis
We have verified the aci treasury address. we have check the amount and the duration are as specified in the description.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.