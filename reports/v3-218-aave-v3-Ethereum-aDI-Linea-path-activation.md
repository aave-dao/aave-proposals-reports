# Proposal 218. a.DI Linea path activation

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=218)

### Governance Forum Discussions
[Link to forum discussions](https://governance.aave.com/t/technical-maintenance-proposals/15274/56)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x3C2A076cD5ECbed55D8Fc0A341c14Fc808bA7fF7)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking

### Context
This proposal revolves around ensuring the seamless activation of the Aave v3 deployment on the Linea network by addressing critical technical prerequisites. Specifically, the proposal aims to register the necessary Linea adapters on the Aave Delivery Infrastructure (a.DI) to enable message passing between Ethereum and Linea. This process mirrors prior technical implementations on networks like Scroll and zkSync, where governance approval of bridge adapter smart contracts was required. By pre-registering the adapter, the proposal ensures that the Linea activation payload can execute smoothly on the network, facilitating the deployment and future cross-chain operations.

### Proposal Creation
Transaction: [0xf00177ebcbfbd49ba620ba34c82ad184128ea0331ed66cb7ab1db8c3d5ee15a4](https://etherscan.io/tx/0xf00177ebcbfbd49ba620ba34c82ad184128ea0331ed66cb7ab1db8c3d5ee15a4)
- `proposalId`: 218
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x6dc4e7ef879555ef1532a33e3701152049ab6850b5dfc7d0c8507bf5f02b8b8d

**`createProposal()` Parameters**
```
{
    "payloads": [
        {
            "chain": "1",
            "accessLevel": 1,
            "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            "payloadId": 221
        }
    ],
    "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    "ipfsHash": "0x6dc4e7ef879555ef1532a33e3701152049ab6850b5dfc7d0c8507bf5f02b8b8d"
}
```

### Aave Seatbelt Report
**Proposal Report**
[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/218.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/221.md)


### Technical Analysis
The analysis confirms that the governance payload in the proposal accurately reflects the technical actions required to register the Linea adapter within the Aave Delivery Infrastructure (a.DI). The specified contract addresses for both Ethereum and Linea have been validated as pre-deployed and correctly configured for their respective roles. The implementation aligns with the need for establishing cross-chain communication, ensuring that the system is ready for the activation of the Aave v3 Linea pool.

The documentation and references provided, including links to codebases and test results, were reviewed and found consistent with the proposal’s objectives. These references demonstrate that the necessary deployment and testing of the adapter have been conducted, supporting the proposal’s readiness for execution. Cross-referencing with similar governance actions for networks like Scroll and zkSync confirms that the process adheres to established standards and practices.

The governance pathway described, including Direct-to-AIP execution, aligns with Aave’s procedural requirements, ensuring that the proposal is properly structured for community approval and execution. The limited scope of the proposal, focused exclusively on the adapter registration, ensures no overreach or unintended functionality is introduced. Overall, the technical and governance aspects of the proposal are sound, with no discrepancies identified that would impede its implementation.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.