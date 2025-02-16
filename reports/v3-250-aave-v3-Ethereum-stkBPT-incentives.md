# Proposal 250. stkBPT Incentives

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=250)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-amend-safety-module-emissions/16640/13)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xDfef791F616AB780f4492E8b8B555BB09BbB1325)



## Certora Analysis

### Proposal Types
* :moneybag: :receipt: Asset transfers

* :wrench: :bar_chart: Configuration updates


### Context
Re-enable stkBPT incentives emissions for 180 days after previous period ended.


### Proposal Creation
Transaction: [0xf07645495d18eee23679740adf10382f98ab8879290dbeb3da4d7538466b612b](https://etherscan.io/tx/0xf07645495d18eee23679740adf10382f98ab8879290dbeb3da4d7538466b612b)
- `proposalId`: 250
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x6a4f2b5540e736107c7ea76d935c9d02edff631359a1785c2f281ee1b046c1f4

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 247,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0x6a4f2b5540e736107c7ea76d935c9d02edff631359a1785c2f281ee1b046c1f4",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/250.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/247.md)


### Technical Analysis
We checked that the amount specified to be distributed each day is as intended. We checked that the distribution end is block.timestamp + 180 days. 

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.