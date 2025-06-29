# Proposal 327. June Funding Update - Part II

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=327)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-june-2025-funding-update/22352/2)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x9E0417be6b9450d8e846e7EeCF65301166019347)



## Certora Analysis

### Proposal Types

* :moneybag: :receipt: Asset transfers
* :handshake: Permission granting and revoking

### Context
This publication presents the June Funding Update, consisting of the following key activities:

- Acquire 3M GHO for Operations;
- Continue AAVE buybacks for 6 weeks; and,
- Create Merit & Ahab Allowances.

### Proposal Creation
Transaction: [0x67557cf3b274800c72b138cf30f32aae1d826ad0cdbc7c346b03da650e16e937](https://etherscan.io/tx/0x67557cf3b274800c72b138cf30f32aae1d826ad0cdbc7c346b03da650e16e937)
- `proposalId`: 327
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x0c6385dcf4f811c09d7e1ce672efe7a471a232461eb15aefc70cc5d6b8367b17

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 306,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x0c6385dcf4f811c09d7e1ce672efe7a471a232461eb15aefc70cc5d6b8367b17",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/327.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/306.md)


### Technical Analysis

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.