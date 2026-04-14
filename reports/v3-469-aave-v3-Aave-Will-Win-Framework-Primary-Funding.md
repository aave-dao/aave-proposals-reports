# Proposal 469. Aave Will Win Framework: Primary Funding Request

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=469)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-aave-will-win-framework/24352)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x59f18C69876ED89F6fE1e103ceDF8E674603b63E)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates
* :bank: Payment stream

### Context
This AIP proposes to approve the primary grant component of the Aave Will Win Framework as a standalone governance action.

If approved, the Aave DAO would fund Aave Labs through various grants consisting of $25,000,000 in stablecoins in totality, alongside a 75,000 AAVE token allocation vesting linearly over four years.

This AIP is limited to the funding request and its full onchain execution. Other elements of the broader framework, including the Growth and Development grants, are intended to be handled through separate governance proposals.

### Proposal Creation
Transaction: [0xd5f0e24c60a2ce434ba895e98a75ba013b3947ec305d608f79e71d4caca8803e](https://etherscan.io/tx/0xd5f0e24c60a2ce434ba895e98a75ba013b3947ec305d608f79e71d4caca8803e)
- `proposalId`: 469
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0x68403758d35bcffdb5f41df8fa9a0500f6bcc0c6eeae801e6627ab2fc8c64727

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 426,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x68403758d35bcffdb5f41df8fa9a0500f6bcc0c6eeae801e6627ab2fc8c64727",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/469.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/426.md)


### Technical Analysis

We have verified the upfront payment and stream amounts, ensuring correct decimal precision.

We have validated the creation of the new streams, confirming their specific durations and deposit amounts.

We have verified that the specified Aave Labs address is correct and designated as the intended recipient.

We have reviewed the payload's logic and successfully validated its execution via Seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.