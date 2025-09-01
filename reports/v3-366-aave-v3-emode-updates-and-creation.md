# Proposal 366. Multi eMode Update and Creation - rsETH, ezETH, wstETH and weETH

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=366)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-arbitrum-emode-update-rseth-and-ezeth/22731/3)

### Payloads

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0x38D7ECF4bC50C8E98dBd1880ab14b091aA5f2Da3)

* Ethereum - [proposal payloads](https://etherscan.io/address/0x02a042E6669919A8f18d17ED9A8F6A65c31045B0)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
This publication proposes updating the ezETH and rsETH eMode categories on Arbitrum, a new wstETH/wETH category on Arbitrum and the creation of weETH <> wstETH eMode on Core.

### Proposal Creation
Transaction: [0xf0ce129e0a34d7afe1e1ef45cff6cd85ed6d806a69f1d23ded4a1cce7ebb9724](https://etherscan.io/tx/0xf0ce129e0a34d7afe1e1ef45cff6cd85ed6d806a69f1d23ded4a1cce7ebb9724)
- `proposalId`: 366
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xfd750a03ca6407a4c5fc62d5751cf46560c40e926cd62bdb52fedbd2b889d577

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 101,
        },
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 335,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xfd750a03ca6407a4c5fc62d5751cf46560c40e926cd62bdb52fedbd2b889d577",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/366.md)

**Payload Reports**

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/101.md)

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/335.md)


### Technical Analysis
We have verified the updated values match the forum and the IPFS, we have confirmed the new emode on core doesn't clash with another new emode in proposal 365, we have checked the proposal for general correctness. 

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.