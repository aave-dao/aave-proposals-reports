# Proposal 450. Create Allowance GHO Mantle

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=450)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-deploy-aave-v3-on-mantle/20542#p-51955-budget-15)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x6F7e0d419E7695Dd6507Be9f58f52abf63485705)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking


### Context
This proposal creates an allowance of 1.5M aEthLidoGHO from the Aave Collector to the Aave Liquidity Committee (ALC) to support the launch of GHO on Mantle.

### Proposal Creation
Transaction: [0xb442a9fc59378ffd1513774af5bc23855d0aed16b4f40e6b39f6d8374c466220](https://etherscan.io/tx/0xb442a9fc59378ffd1513774af5bc23855d0aed16b4f40e6b39f6d8374c466220)
- `proposalId`: 450
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x45f732e300bc75c5d41062e3454a06e2ad45306520685e4c3d5b4cfdfc99a3a7

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 405,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x45f732e300bc75c5d41062e3454a06e2ad45306520685e4c3d5b4cfdfc99a3a7",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/450.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/405.md)


### Technical Analysis
We have verified that an allowance of 1,500,000 aEthLidoGHO was correctly granted from the Aave Collector to the Aave Liquidity Committee.

We validated the payload logic and confirmed execution via Seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.