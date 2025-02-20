# Proposal 253. Caps Risk Oracle Activation on Arbitrum

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=253)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-supply-and-borrow-cap-risk-oracle-activation/20834)

### Payloads

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0xC3e81AC1b817744db2829b1F51340BcAE88E6483)



## Certora Analysis

### Proposal Types
* :moneybag: :receipt: Asset transfers

* :handshake: Permission granting and revoking


### Context
This proposal activates the automated Aave Generalized Risk Stewards (AGRS) system on the Arbitrum Instance to perform automated supply and borrow cap updates. Under the hood, the AGRS consumes risk recommendations from the Edge infrastructure by Chaos Labs.

### Proposal Creation
Transaction: [0x2a356d8ddfc194f8312a71129a3379023c2e9c9d104e36e7b63bae9d90afe92e](https://etherscan.io/tx/0x2a356d8ddfc194f8312a71129a3379023c2e9c9d104e36e7b63bae9d90afe92e)
- `proposalId`: 253
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x3a9e0990b0c828e0af7b602f29273c4166a628d8b2249896fac69c12cc8f7b5a

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 75,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0x3a9e0990b0c828e0af7b602f29273c4166a628d8b2249896fac69c12cc8f7b5a",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/253.md)

**Payload Reports**

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/75.md)


### Technical Analysis
We have verified that the stated addresses are the upgraded contracts. We have verified the transfer of 50 LINK and confirmed that the registering mechanism works as intended.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.