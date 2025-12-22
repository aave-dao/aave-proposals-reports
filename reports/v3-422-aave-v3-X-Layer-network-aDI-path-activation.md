# Proposal 422. X Layer network aDI path activation

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=422)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/technical-maintenance-proposals/15274/120)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x90345B3f6d25684EB921c056Fad6CCf6360ceA5B)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking



### Context
Proposal to register the necessary XLayer adapters on a.DI, a technical pre-requirement for an activation vote of Aave v3 XLayer. In order to be able to pass messages from Ethereum to XLayer via a.DI (Aave Delivery Infrastructure), it is necessary to at least have one valid adapter Ethereum → XLayer smart contract enabled in the system (native adapter).
The first case of message passing Ethereum → XLayer is the activation proposal for an Aave v3 XLayer pool and consequently, to be able to execute on the XLayer side the payload, the Aave governance should approve in advance the a.DI adapters smart contracts.

### Proposal Creation
Transaction: [0x61900eb166d3287079989647b1dd2eb7dde1123dc9e70045677fd2b688e7a29a](https://etherscan.io/tx/0x61900eb166d3287079989647b1dd2eb7dde1123dc9e70045677fd2b688e7a29a)
- `proposalId`: 422
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x413ba4c68088e7a7f4c299a3897bd3f7f1a6d525dfd3cb344a45c318853113f0

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 379,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x413ba4c68088e7a7f4c299a3897bd3f7f1a6d525dfd3cb344a45c318853113f0",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/422.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/379.md)


### Technical Analysis
We have verified alignment between the Forum and IPFS.
We have verified that the addresses supplied to the constructor are correct.
We have checked all X Layer addresses and their implementations.
The Governance Guardian is set as the guardian of the PayloadsController, and the `CROSS_CHAIN_CONTROLLER` address is correct.
The Granular Guardian is set as the guardian of the CrossChainController.
The BGD Labs Guardian is set to the RETRY_ROLE.
The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.