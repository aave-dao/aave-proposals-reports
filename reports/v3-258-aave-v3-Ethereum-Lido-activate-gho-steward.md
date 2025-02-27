# Proposal 258. Extend GHO Steward on Aave Prime Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=258)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-extend-gho-steward-on-aave-prime-instance/20598)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x4b0f509ab3E07dE8984E45c37678a9C650234B61)



## Certora Analysis

### Proposal Types
* :handshake: Permission granting and revoking

### Context
Following the development of the Gho steward and it's utilization on Arbitrum, this proposal seek to apply the steward on the Ethereum Prime (Lido) instance to manage the Gho token.

### Proposal Creation
Transaction: [0xaee69532b473701cd2b3b14ec007396735aab17a67504860786cff3edc77b3c7](https://etherscan.io/tx/0xaee69532b473701cd2b3b14ec007396735aab17a67504860786cff3edc77b3c7)
- `proposalId`: 258
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x8e8859a1ce499fdd4285610e9a833daf66da59c57af40469bad8aa110d33db88

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 251,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0x8e8859a1ce499fdd4285610e9a833daf66da59c57af40469bad8aa110d33db88",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/258.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/251.md)


### Technical Analysis
We verified that the contract granted risk admin role is indeed the official aave-steward role. In addition, the old and currently used risk steward was restricted from managing the Gho token.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.