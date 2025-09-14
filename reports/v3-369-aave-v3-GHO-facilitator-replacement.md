# Proposal 369. GHO Facilitator Replacement

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=369)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/technical-maintenance-proposals/15274/107)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xfc9116C5Bc78E9f78A7Ce2ecc0D58d1c0Bfb6410)



## Certora Analysis

### Proposal Types

* :scroll: :small_red_triangle: Contract upgrades

### Context
This proposal outlines the migration from the current CoreGhoDirectMinter to a new, correctly configured instance.

### Proposal Creation
Transaction: [0x37ce2006ca1dbfb3f8e7506e4c0a80351db17036c370535fe01515c2e27cc2a1](https://etherscan.io/tx/0x37ce2006ca1dbfb3f8e7506e4c0a80351db17036c370535fe01515c2e27cc2a1)
- `proposalId`: 369
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x2415ac8bb2cbbe7b2392920e31e897221652da9d68ea3028fca8ef9473098243

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 336,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x2415ac8bb2cbbe7b2392920e31e897221652da9d68ea3028fca8ef9473098243",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/369.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/336.md)


### Technical Analysis
We have reviewed and confirmed the safety of the upgrade. The old facilitator issue has been fixed, the bucket level stays the same for the new facilitator. The old facilitator have been disabled correctly. We have communicated on the [forum](https://governance.aave.com/t/technical-maintenance-proposals/15274/110?) our assessment of this proposal.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.