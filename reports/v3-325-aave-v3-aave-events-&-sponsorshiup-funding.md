# Proposal 325. Aave Events & Sponsorship Budget 2025

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=325)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-aave-events-sponsorship-budget-2025/22173)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xf58c30F316E3b8200cbc83365e7E1f7F648dC5C9)



## Certora Analysis

### Proposal Types

* :moneybag: :receipt: Asset transfers


### Context
Aave Labs is requesting a grant for $750,000 paid in GHO for events in 2025 to be transferred to [0x1c037b3C22240048807cC9d7111be5d455F640bd](https://etherscan.io/address/0x1c037b3C22240048807cC9d7111be5d455F640bd) from the 'Ethereum Collector'

### Proposal Creation
Transaction: [0x72751f30d50f8bd0a57f8266200691fa8053a66efd5b1c4a01504f465e93e194](https://etherscan.io/tx/0x72751f30d50f8bd0a57f8266200691fa8053a66efd5b1c4a01504f465e93e194)
- `proposalId`: 325
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xa4f30894edb67f82e16ba763e04fcb1a4f613b8d17fa0ecbaa872b1ba4adeab0

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 303,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xa4f30894edb67f82e16ba763e04fcb1a4f613b8d17fa0ecbaa872b1ba4adeab0",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/325.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/303.md)


### Technical Analysis

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.