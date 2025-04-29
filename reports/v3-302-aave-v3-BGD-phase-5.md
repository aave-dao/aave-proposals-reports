# Proposal 302. Aave BGD Phase 5

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=302)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-aave-bored-ghosts-developing-phase-5/21803)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x1a801efEE82a50F7Bb864148cdA233CA76b20B36)



## Certora Analysis

### Proposal Types

* :bank: Payment stream

### Context
Proposal for an engagement of development and security services between the Aave DAO and BGD Labs, from 1st April 2025 until 1st October 2025.

### Proposal Creation
Transaction: [0x0ff2757e14bc10f28507038e068090ba0fdf4b073138c76c3654fddb09f360a2](https://etherscan.io/tx/0x0ff2757e14bc10f28507038e068090ba0fdf4b073138c76c3654fddb09f360a2)
- `proposalId`: 302
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x510feeec05cecc90e051a33a8b0f78808b39971199da61d4f50dc8ced6cf74aa

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 280,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x510feeec05cecc90e051a33a8b0f78808b39971199da61d4f50dc8ced6cf74aa",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/302.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/280.md)


### Technical Analysis
We have verified the receiving address, the amount sent upfront (with respect to scailing) and the duration of the streams.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.