# Proposal 404. Aave BGD Phase 6 & Project E agreement

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=404)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-aave-bored-ghosts-developing-phase-6/23191)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x65e22E0dd3E0d53cD07E7EA446A8f5139a3C87E9)



## Certora Analysis

### Proposal Types

* :bank: Payment stream

### Context
Present to the Aave DAO a proposal from BGD Labs to renew our involvement as a development and security coordinator services provider until 1st April 2026 (previous finished 1st October 2025). Additionally, presenting a new BGD project line that will partially use Aave licensed technology: (codename) Project E.

### Proposal Creation
Transaction: [0x517103f901a256292827fa3f8d6cd6113134e1e46b1f162fc6b16d4507eb7ac6](https://etherscan.io/tx/0x517103f901a256292827fa3f8d6cd6113134e1e46b1f162fc6b16d4507eb7ac6)
- `proposalId`: 404
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x8255c95514402a834f32b4fa19e61250219f2c4e0b75bce3389f457234124f0d

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 367,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x8255c95514402a834f32b4fa19e61250219f2c4e0b75bce3389f457234124f0d",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/404.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/367.md)


### Technical Analysis
We have confirmed alignment between the forum post, the IPFS content, and the on-chain payload.
We validated the addresses, unix timestamp and the amounts, including decimal-precision checks, and confirmed that the payload logic is correct and will execute as intended.
We also validated the execution using Seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.