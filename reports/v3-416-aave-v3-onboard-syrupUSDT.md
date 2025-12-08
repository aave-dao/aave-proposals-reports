# Proposal 416. Onboard syrupUSDT to Aave V3 Core Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=416)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-onboard-syrupusdt-to-aave-v3-core-instance/23291)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x82E401633b26e49628BE8563bC874597a8CB8db8)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets

### Context
This proposal seeks to onboard syrupUSDT to Aave V3 Core Instance.

### Proposal Creation
Transaction: [0x6776733a9ff0ed10a60a1a6c843e937aaf8d7ab9c7cb8d83482dacd1acafd5bb](https://etherscan.io/tx/0x6776733a9ff0ed10a60a1a6c843e937aaf8d7ab9c7cb8d83482dacd1acafd5bb)
- `proposalId`: 416
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x48d70d4984cfef8f9b6c3901d6d19abc87e90ece33d206005b709424021a7628

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 375,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x48d70d4984cfef8f9b6c3901d6d19abc87e90ece33d206005b709424021a7628",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/416.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/375.md)


### Technical Analysis
The proposal is consistent with the description on both Snapshot and the governance forum. We have checked the alignment of the risk parameters against the risk providers’ parameters. We have verified the payload logic and checked its execution via Seatbelt. We have verified the token address and the LM_ADMIN address. We have validated the supply amount with respect to decimal precision.
### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.