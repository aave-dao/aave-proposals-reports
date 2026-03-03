# Proposal 453. GSM Migration

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=453)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-launch-gho-on-plasma-set-aci-as-emissions-manager-for-rewards/22994/8)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x57eA078d14b7EbC7243c1b7be847A5d3ACdbfFa3)



## Certora Analysis

### Proposal Types

* :scroll: :small_red_triangle: Contract upgrades
* :moneybag: :receipt: Asset transfers
* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates



### Context
With the launch of what is known as the new Remote GSM, this publication updates the existing Mainnet GSMs to the new version.
To create a unified GSM paradigm for both mainnet and L2s, a newer version of the GSM has been developed. The new GSMs use and restore GHO to a DAO controlled GhoReserve that holds a predefined amount of GHO and the DAO allows entities (such as the GSMs) to draw GHO up to a predefined amount.

### Proposal Creation
Transaction: [0x5a494dfd587667dff394d3f1b94b22a569e4deaca3eeed71a2c4fe0a9a17fb89](https://etherscan.io/tx/0x5a494dfd587667dff394d3f1b94b22a569e4deaca3eeed71a2c4fe0a9a17fb89)
- `proposalId`: 453
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xcebaf994554764db9c9aa08c6908f8f2e31bf98e785f7bdbe4b05df93eea7199

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 408,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xcebaf994554764db9c9aa08c6908f8f2e31bf98e785f7bdbe4b05df93eea7199",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/453.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/408.md)


### Technical Analysis

We audited the new GSM by `TokenLogic`.
We confirm that the payload is the exact version we audited. 

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.