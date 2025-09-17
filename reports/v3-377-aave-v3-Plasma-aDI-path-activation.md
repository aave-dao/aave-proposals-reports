# Proposal 377. Plasma aDI path activation

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=377)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/technical-maintenance-proposals/15274/112)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xBD770E618C49d151959d596D5d2770F0f3301a7b)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking


### Context
Proposal to register the necessary Plasma adapters on a.DI, a technical pre-requirement for an activation vote of Aave v3 Plasma.

### Proposal Creation
Transaction: [0x7495944393932fd911ea72313108a54544c5426cd900ac2b0e76afa846be9caa](https://etherscan.io/tx/0x7495944393932fd911ea72313108a54544c5426cd900ac2b0e76afa846be9caa)
- `proposalId`: 377
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x9694aa29e59ff10b11cc465cf7abc214a98866daecad2792e869f67c99629c1c

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 342,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x9694aa29e59ff10b11cc465cf7abc214a98866daecad2792e869f67c99629c1c",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/377.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/342.md)


### Technical Analysis
The analysis confirms that the governance payload in the proposal accurately reflects the technical actions required to register the `Plasma` adapter within the Aave Delivery Infrastructure (a.DI). The specified contract addresses for both Ethereum and Plasma have been validated as pre-deployed and correctly configured for their respective roles. The implementation aligns with the need for establishing cross-chain communication, ensuring that the system is ready for the activation of the Aave v3 Plasma pool.

The documentation and references provided, including links to codebases and test results, were reviewed and found consistent with the proposal’s objectives. These references demonstrate that the necessary deployment and testing of the adapter have been conducted, supporting the proposal’s readiness for execution. Cross-referencing with similar governance actions for networks like Linea and Sonic confirms that the process adheres to established standards and practices.

The governance pathway described, including Direct-to-AIP execution, aligns with Aave’s procedural requirements, ensuring that the proposal is properly structured for community approval and execution. The limited scope of the proposal, focused exclusively on the adapter registration, ensures no overreach or unintended functionality is introduced. Overall, the technical and governance aspects of the proposal are sound, with no discrepancies identified that would impede its implementation.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.