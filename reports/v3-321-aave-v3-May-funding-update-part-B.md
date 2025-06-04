# Proposal 321. May Funding Part B

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=321)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-may-2025-funding-update/21906/5)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x82c8ae8c6B4E722Df152236C063227B2f2Dc2095)

* Base - [proposal payloads](https://basescan.org/address/0xcb0d1e4FF9e23e93cd3135ccB20711D6C9767462)



## Certora Analysis

### Proposal Types

* :moneybag: :receipt: Asset transfers

* :handshake: Permission granting and revoking

* :bank: Payment stream

### Context
This publication finalizes the May Funding Update and provides the funding required to support the upcoming Base Incentive Campaign, which includes the following key components:

- Allocation for Base Incentive Campaign allowances;
- Allowances for Merit and Ahab contributors; and,
- Consolidation of funds from the Collector.

### Proposal Creation
Transaction: [0x1996dd476995cc7f8870dede52a7ce43bf19c0f0b1ed3b4e4050e869f56e70b5](https://etherscan.io/tx/0x1996dd476995cc7f8870dede52a7ce43bf19c0f0b1ed3b4e4050e869f56e70b5)
- `proposalId`: 321
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x3620c2aad3bf4e7dc5d9fda5c27592c60f78125b90b79535f4371b69645cdbcb

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 296,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 72,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x3620c2aad3bf4e7dc5d9fda5c27592c60f78125b90b79535f4371b69645cdbcb",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/321.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/296.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/72.md)


### Technical Analysis
We have validated the recipient addresses, the correct amounts with respect to precision and that the new stream was configured correctly.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.