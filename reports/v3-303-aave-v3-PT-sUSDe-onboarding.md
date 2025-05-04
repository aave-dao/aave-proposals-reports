# Proposal 303. Onboard PT sUSDe July on Core Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=303)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-onboard-susde-july-expiry-pt-tokens-on-aave-v3-core-instance/21878)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xcA6B2Dbf0c41504887cc80EBd8948908992A4E2c)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context
This proposal seeks to onboard pendle PT-sUSDe-31July2025 on the Aave V3 core instance.
This is a resubmission of PT-sUSDe-31July2025 listing payload of [Proposal 299](https://vote.onaave.com/proposal/?proposalId=299), which was cancelled due to a detected misconfiguration.

### Proposal Creation
Transaction: [0xaeafb831bea6c497b6589e3d6feb107bff7f8a826fae617d4fde6767f946cbcd](https://etherscan.io/tx/0xaeafb831bea6c497b6589e3d6feb107bff7f8a826fae617d4fde6767f946cbcd)
- `proposalId`: 303
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xc0e9c24f7279bec1d6735560184c11f298b1c4c6cd22238549bbc60017a070d7

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 281,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xc0e9c24f7279bec1d6735560184c11f298b1c4c6cd22238549bbc60017a070d7",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/303.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/281.md)


### Technical Analysis
We have validated the price oracle is configured correctly with the right price feeds. We have compared the risk parameters between the IPFS the forum and the payload and found no incompatibilities.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.