# Proposal 291. Removal of legacy VotingPortals from Governance v3

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=291)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/technical-maintenance-proposals/15274/77)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x7DC3c515eE86DE450DdB3b8DDfB497c5b41Da7af)

## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
Proposal to remove the deprecated VotingPortals from the Aave Governance.

As the new VotingPortals have already been proven to be working by using them for voting on at least 4 new proposals (279 - 282), it is time to remove the old ones, so that there is no confusion or possibility of using the old VotingPortals on new proposals.


### Proposal Creation
Transaction: [0xec6704638e704b24144ba95e7ee64f2127405f668e49f3c16110b423a5a032dc](https://etherscan.io/tx/0xec6704638e704b24144ba95e7ee64f2127405f668e49f3c16110b423a5a032dc)
- `proposalId`: 291
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x2976c79737ef0a16930cab6eea90bf53c157fe01d9a3a904f435f266a4dddcf5

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 269,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x2976c79737ef0a16930cab6eea90bf53c157fe01d9a3a904f435f266a4dddcf5",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/291.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/269.md)


### Technical Analysis
We have checked that only the deprecated portals have removed.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.