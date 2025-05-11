# Proposal 307. stkGHO Emissions

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=307)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-amend-safety-module-emissions/16640/18)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x3b13084cEB8E3E8099E26C494346d24Ff60ef302)



## Certora Analysis

### Proposal Types

* :moneybag: :receipt: Asset transfers
* :handshake: Permission granting and revoking

### Context
Re-enable stkGHO incentives emissions for 180 days after previous period ended.

### Proposal Creation
Transaction: [0xbb28114d65e03b13a6a58c304f01f150c8af4fccf14d80f71e42f501fc03d63b](https://etherscan.io/tx/0xbb28114d65e03b13a6a58c304f01f150c8af4fccf14d80f71e42f501fc03d63b)
- `proposalId`: 307
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xb8df479b7c12b6a8a00eb98be25079f2255d2796f2af969513901414eac85c2d

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 286,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xb8df479b7c12b6a8a00eb98be25079f2255d2796f2af969513901414eac85c2d",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/307.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/286.md)


### Technical Analysis
We have verified the allowance was configured to the exact amount that intended. We hav e validated the end time of the distribution is to 180 days from execution day.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.