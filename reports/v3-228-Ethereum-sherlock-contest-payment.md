# Proposal 228. Aave v3.3 Sherlock contest funding

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=228)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-bgd-aave-v3-3-sherlock-contest/20498)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x991200058D0abfa279192a9b3575D9A679BBBDBb)



## Certora Analysis

### Proposal Types
* :moneybag: :receipt: Asset transfers

### Context
Following all technical development and ordinary security procedures for the Aave V3.3 upgrade, it was decided to complement the security process with a sherlock contest.

### Proposal Creation
Transaction: [0x9227a4666c1ad4eb2f5a398c5d2ffc47b43c846bc1ae8917f5f9382a9711bf70](https://etherscan.io/tx/0x9227a4666c1ad4eb2f5a398c5d2ffc47b43c846bc1ae8917f5f9382a9711bf70)
- `proposalId`: 228
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0xf4899816147eb97bdf4630a9ad1bec2c1266e612094e0a744a9bc264c304945c

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 230,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0xf4899816147eb97bdf4630a9ad1bec2c1266e612094e0a744a9bc264c304945c",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/228.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/230.md)


### Technical Analysis
The payload withdraws a total of 230k USDC from the Ethereum collector and transfers it as specified in the IPFS:
- 30k to BGDLabs
- 200k to Sherlock

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.