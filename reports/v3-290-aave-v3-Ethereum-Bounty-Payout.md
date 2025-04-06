# Proposal 290. Request for Bounty Payout - March 2025

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=290)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/bgd-request-for-bounty-payout-march-2025/21656)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x160A00C878c56d9Cb0739B676D358d33ee5409B8)



## Certora Analysis

### Proposal Types

* :moneybag: :receipt: Asset transfers


### Context
Proposal to release a total of $21’000 as bounty for four outstanding Aave <> Immunefi valid submissions, together with $2’100 as the fee to the Immunefi platform; amounting to a grand total of $23'100.

### Proposal Creation
Transaction: [0xab34e3a5986cac34270ff775f57ed10d2990a9d6b6ecfa9456ac63f05c080fcd](https://etherscan.io/tx/0xab34e3a5986cac34270ff775f57ed10d2990a9d6b6ecfa9456ac63f05c080fcd)
- `proposalId`: 290
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x65a2b1557732fc00eeee947ab9bbbe3b3adfa3da7ff0a5e7203cd748c18b7fe6

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 268,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x65a2b1557732fc00eeee947ab9bbbe3b3adfa3da7ff0a5e7203cd748c18b7fe6",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/290.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/268.md)


### Technical Analysis
We have the correct amounts with the right precision were transferred to the intended addresses.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.