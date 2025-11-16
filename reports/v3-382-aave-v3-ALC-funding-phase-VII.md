# Proposal 382. Aave Liquidity Committee Funding Phase VII

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=382)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-aave-liquidity-committee-funding-phase-vii/23143)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x2A628Da62926a430533941f97e1aC720eFB0c54e)



## Certora Analysis

### Proposal Types

* :moneybag: :receipt: Asset transfers

* :handshake: Permission granting and revoking


### Context
This proposal presents the Aave Liquidity Committee (ALC) Phase VII Funding request. Since the last update in April, GHO has experienced significant growth across supply, integrations, and ecosystem adoption. This proposal seeks to sustain and accelerate that momentum while lowering the overall budget requirements compared to the previous phase.

### Proposal Creation
Transaction: [0xe89218ceeabcb30a82d6a2e3bbb316d04c65140194e43b98ee3ce7b1cfcc3f42](https://etherscan.io/tx/0xe89218ceeabcb30a82d6a2e3bbb316d04c65140194e43b98ee3ce7b1cfcc3f42)
- `proposalId`: 382
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x32e370abd40501a77ccf10f3b822654a33b54eef42cffb092662da6634473bb6

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 350,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x32e370abd40501a77ccf10f3b822654a33b54eef42cffb092662da6634473bb6",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/382.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/350.md)


### Technical Analysis
We have validated the approve is from 0 amount to the specified correct amount. We have check the `to` address to match the proposal description, we have validated the decimal precision for correctness.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.