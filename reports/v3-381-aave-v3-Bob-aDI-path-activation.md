# Proposal 381. Bob Network aDI path activation

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=381)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/technical-maintenance-proposals/15274/114)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xb46874c48b8F1d7303bC40F1c9E4bB4f159FCCf9)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking

### Context
Proposal to register the necessary Bob adapters on a.DI, a technical pre-requirement for an activation vote of Aave v3 Bob.


### Proposal Creation
Transaction: [0xaf71a2484ee0af90fd383904298c9b928f3e2e630b38cd11aec7658bc1638af5](https://etherscan.io/tx/0xaf71a2484ee0af90fd383904298c9b928f3e2e630b38cd11aec7658bc1638af5)
- `proposalId`: 381
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0xc15d0f4a7513053f07b25e237bd3f22b1a30b53100a4e31f06234fd9b533234e

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 346,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xc15d0f4a7513053f07b25e237bd3f22b1a30b53100a4e31f06234fd9b533234e",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/381.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/346.md)


### Technical Analysis
The analysis confirms that the governance payload in the proposal accurately reflects the technical actions required to register the `Bob` adapter within the Aave Delivery Infrastructure (a.DI). The specified contract addresses for both Ethereum and Bob have been validated as pre-deployed and correctly configured for their respective roles. The implementation aligns with the need for establishing cross-chain communication, ensuring that the system is ready for the activation of the Aave v3 Bob pool.

The documentation and references provided, including links to codebases and test results, were reviewed and found consistent with the proposal’s objectives. These references demonstrate that the necessary deployment and testing of the adapter have been conducted, supporting the proposal’s readiness for execution. Cross-referencing with similar governance actions for networks like Linea and Sonic confirms that the process adheres to established standards and practices.

The governance pathway described, including Direct-to-AIP execution, aligns with Aave’s procedural requirements, ensuring that the proposal is properly structured for community approval and execution. The limited scope of the proposal, focused exclusively on the adapter registration, ensures no overreach or unintended functionality is introduced. Overall, the technical and governance aspects of the proposal are sound, with no discrepancies identified that would impede its implementation.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.