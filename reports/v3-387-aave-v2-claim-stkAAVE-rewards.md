# Proposal 387. Claim Aave v2 stkAAVE rewards

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=387)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/technical-maintenance-proposals/15274/115)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x95D98A409Bd14A35150aa4dC5A43DE797001F90F)

* Ethereum - [proposal payloads](https://etherscan.io/address/0xd6fF119A67A33725a28852eFd5055E72Cb92C48f)



## Certora Analysis

### Proposal Types

* :moneybag: :receipt: Asset transfers

* :handshake: Permission granting and revoking


### Context
Maintenance proposal to claim unclaimed StkAave rewards from the Ethereum V2 Incentives Controller.


### Proposal Creation
Transaction: [0x53c1f3d920af3e69e6bf9cb4cb08e4c3b599026f74d19c56e07b8eb314191142](https://etherscan.io/tx/0x53c1f3d920af3e69e6bf9cb4cb08e4c3b599026f74d19c56e07b8eb314191142)
- `proposalId`: 387
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x1d0be03af9546300dafa1794f97d82abe6a84d8bfd47d535e2eb38751018598f

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 355,
        },
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 356,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x1d0be03af9546300dafa1794f97d82abe6a84d8bfd47d535e2eb38751018598f",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/387.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/355.md)

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/356.md)


### Technical Analysis
We have thoroughly check the unique procedure the proposal introduce. We have verified the queue and execution procedure will executed seamlessly. We have verified that only `stkAAVE` rewards are claimed and no other action was introduced

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.