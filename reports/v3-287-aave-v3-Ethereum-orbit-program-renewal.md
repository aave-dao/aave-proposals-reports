# Proposal 287. Orbit Program Renewal

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=287)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-orbit-program-renewal-q1-2025/21205)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x4eD1EfE307b784B3E9b72A50AbA0dFAd3B14fD43)


## Certora Analysis

### Proposal Types
* :bank: Payment stream

### Context
Proposing the renewal of the Orbit program for recognized delegates, compensating them with GHO, associated with their governance activity during Q1 2025 ( From 2024-12-14, last date, until 2025-03-31).

### Proposal Creation
Transaction: [0xbf9e1374ad41bebe56561a4f9e85af151f2324833d8d766202fd5a9900ec0f76](https://etherscan.io/tx/0xbf9e1374ad41bebe56561a4f9e85af151f2324833d8d766202fd5a9900ec0f76)
- `proposalId`: 287
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x1f1715ca8bef5fe45d423c093e7b6e1aeb6dc6598d393d6ce5058c62acc65812

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 264,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x1f1715ca8bef5fe45d423c093e7b6e1aeb6dc6598d393d6ce5058c62acc65812",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/287.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/264.md)


### Technical Analysis
We have confirmed the correct amount to the correct addresses were renewed the stream to the correct period of time.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.