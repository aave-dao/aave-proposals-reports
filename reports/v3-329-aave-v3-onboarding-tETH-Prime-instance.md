# Proposal 329. Onboard tETH to Aave v3 Prime Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=329)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-onboard-teth-to-aave-v3-prime-instance/21873)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x61D0DCB050507Fe82459f5b114063F4000D98B3E)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context
This proposal aims to onboard tETH to Aave V3 Prime Instance.

### Proposal Creation
Transaction: [0xa9cd00ed098b7b2de59c82aeebe7560fd6eed1685da852394edbd748e0c7ebf9](https://etherscan.io/tx/0xa9cd00ed098b7b2de59c82aeebe7560fd6eed1685da852394edbd748e0c7ebf9)
- `proposalId`: 329
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x53f0deb5b4edb43d2a297caad540900bc6a359ade80aefe519164a8d83059364

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 308,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x53f0deb5b4edb43d2a297caad540900bc6a359ade80aefe519164a8d83059364",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/329.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/308.md)


### Technical Analysis

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.