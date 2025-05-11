# Proposal 305. Onboard USDtb to Aave v3 Core Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=305)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-onboard-usdtb-to-aave-v3-core-instance/21746)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xaffE7Ae0dF52d983A8cD80A118EBBBC278f0B896)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context
Onboard USDtb to the v3 Core Instance with borrow enabled, collateral disabled.

### Proposal Creation
Transaction: [0x1702083786b7f2729abf7094d6357be9c6c81cb3e450f1d5ea82c08df2c62352](https://etherscan.io/tx/0x1702083786b7f2729abf7094d6357be9c6c81cb3e450f1d5ea82c08df2c62352)
- `proposalId`: 305
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x17c8aab4e08a5f6148b7358a29b01af5404018773bb4715f5440c23ab8a83e7f

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 284,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x17c8aab4e08a5f6148b7358a29b01af5404018773bb4715f5440c23ab8a83e7f",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/305.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/284.md)


### Technical Analysis
There was a small discrepancy between what specified in the IPFS specification to the forum and payload. The field collateral enabled  was configured to true although it is suppose to be false. 

Other than that all risk parameters match and the price feed configured correctly.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.