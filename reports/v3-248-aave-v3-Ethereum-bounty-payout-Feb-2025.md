# Proposal 248. Request for Bounty Payout - Feb 2025

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=248)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/bgd-request-for-bounty-payout-january-2025/20947)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x4D446f341fEbf0b7eF137e603DfEc2560Cf39Dab)



## Certora Analysis

### Proposal Types

* :moneybag: :receipt: Asset transfers

### Context
Proposal to release a total of $61’000 as bounty for four outstanding Aave <> Immunefi valid submissions, together with $6’100 as the fee to the Immunefi platform; amounting to a grand total of $67’100.

### Proposal Creation
Transaction: [0x735793d7c90912bc69db047219583392ae496e533642bda1aa29db30597c021f](https://etherscan.io/tx/0x735793d7c90912bc69db047219583392ae496e533642bda1aa29db30597c021f)
- `proposalId`: 248
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x1b4eb9f586cbb44071b16526737d779953b1a53b057db65987aa9f084674a953

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 245,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0x1b4eb9f586cbb44071b16526737d779953b1a53b057db65987aa9f084674a953",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/248.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/245.md)


### Technical Analysis
We have reviewed the addresses and amounts are as specified in the ipfs and forum.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.