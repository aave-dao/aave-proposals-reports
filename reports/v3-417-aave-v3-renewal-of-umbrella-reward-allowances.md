# Proposal 417. Renewal of Umbrella Reward Allowances

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=417)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-renewal-of-umbrella-reward-allowances/23474)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xF861E633BEd1fcDFa534ef7fEC8E30be7D3B0959)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates


### Context
This proposal renews the Umbrella reward allowances to support continuing to distribute emissions at the current rate without any disruption to user positions.

### Proposal Creation
Transaction: [0x45b08ae250141fd5e7263f3e3f6d321d657745c16767530091201a26880d2e34](https://etherscan.io/tx/0x45b08ae250141fd5e7263f3e3f6d321d657745c16767530091201a26880d2e34)
- `proposalId`: 417
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x7e706b3bfc13025cdc8873bd6f45d6808fb7a1a2ac6203340d3f93bc0c1ca5e6

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 376,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x7e706b3bfc13025cdc8873bd6f45d6808fb7a1a2ac6203340d3f93bc0c1ca5e6",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/417.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/376.md)


### Technical Analysis
Proposal payload wasn’t verified at creation. we reached out to ACI and asked them to verify it. Before verification, we checked the execution via Seatbelt and the implementation. We have validated consistency in the allowance renewal amounts between the forum, IPFS, implementation, and the payload after verification, all with respect to decimal precision. We have flagged that LlamaRisk suggested a different renewal amount for `stkwaEthUSDT.v1`. 
We have validated payload's execution logic.
The proposal is consistent with the description on both Snapshot and the governance forum.



### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.