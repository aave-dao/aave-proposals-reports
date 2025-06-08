# Proposal 322. Asset Parameters Optimization

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=322)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-asset-parameters-optimization/22178)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x40a021449327b5e41Ec55b8B020A8c71Db2b567B)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x079B53AfdaD89a294590a459e2b677b21251cEe5)

* Celo - [proposal payloads](https://celo.blockscout.com/address/0x85981D8f89Ea0E6caB9f14B1285EAE664EBDfA87)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates



### Context
This proposal aims to optimize parameters of certain assets across networks where it is supported.

### Proposal Creation
Transaction: [0xdb7d34479cd1e99327c3a9fd806b1df4fe420eb07e2a820e07669b319555f5b3](https://etherscan.io/tx/0xdb7d34479cd1e99327c3a9fd806b1df4fe420eb07e2a820e07669b319555f5b3)
- `proposalId`: 322
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xd88fe280b6079d50ab9a283cc4c5ae52c90fdb3d50b8bec4d3cbb65b350d687f

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 297,
        },
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 113,
        },
        {
            chain: "42220",
            payloads_controller: "0xE48E10834C04E394A04BF22a565D063D40b9FA42",
            payload_id: 5,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xd88fe280b6079d50ab9a283cc4c5ae52c90fdb3d50b8bec4d3cbb65b350d687f",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/322.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/297.md)

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/113.md)

* Celo - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42220/0xE48E10834C04E394A04BF22a565D063D40b9FA42/5.md)


### Technical Analysis
We have verified the specified risk parameters are configured as specified on the IPFS and forum.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.