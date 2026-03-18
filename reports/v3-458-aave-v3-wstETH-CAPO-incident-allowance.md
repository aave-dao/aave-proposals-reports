# Proposal 458. wstETH CAPO Oracle Incident User Reimbursement

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=458)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-wsteth-capo-oracle-incident-user-reimbursement/24275)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x3EF2AE34F825BBd4367D5d5AE90c763941059429)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking


### Context
{**TODO: Write context.**}

### Proposal Creation
Transaction: [0x8f53fd1790a98a4a8c3ad3f674fa9fec7fe75860efb0577333afca0f8544b1c0](https://etherscan.io/tx/0x8f53fd1790a98a4a8c3ad3f674fa9fec7fe75860efb0577333afca0f8544b1c0)
- `proposalId`: 458
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x92ff1fa304a74fcbfcf5d5829bf18110f44ce187182bd9845a3951d371544a45

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 413,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x92ff1fa304a74fcbfcf5d5829bf18110f44ce187182bd9845a3951d371544a45",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/458.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/413.md)


### Technical Analysis
We have validated the approved token, amount, and spender matches the IPFS and forum. We have checked seatbelt to see state changed and only the specify allowance was created correctly.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.