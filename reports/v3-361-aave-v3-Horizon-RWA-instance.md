# Proposal 361. Horizon RWA Instance Activation

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=361)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-horizon-s-rwa-instance/21898)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x2082f5234722A1D538c585F142013Bf7f41774dd)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking


### Context
Proposal to activate the Horizon RWA instance on mainnet

### Proposal Creation
Transaction: [0x1a0ed002b253ee4bef50329e9560339b9e1edc91781a071ce90e6b8a064fe6d1](https://etherscan.io/tx/0x1a0ed002b253ee4bef50329e9560339b9e1edc91781a071ce90e6b8a064fe6d1)
- `proposalId`: 361
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0x233c5510aa9aea7789aa08f3b6ae749806a1c3e2734d3487faeb6a8aa3007e69

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 331,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x233c5510aa9aea7789aa08f3b6ae749806a1c3e2734d3487faeb6a8aa3007e69",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/361.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/331.md)


### Technical Analysis
We have made a security assessment to the proposal and posted a report, more over we a have reviewed th proposal, validated addresses and confirm the overall logic is correct.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.