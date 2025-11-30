# Proposal 415. Add MetaMask USD (mUSD) to Aave V3 Ethereum/Linea

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=415)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-add-metamask-usd-musd-to-aave-v3-core-instance-on-ethereum-and-linea/23097)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x9ED5BfdBA709318a1d7AAf6644D20Fa4497Dc14f)

* Linea - [proposal payloads](https://lineascan.build/address/0xAf246E4A133E95Fcf8F8BEF5a4509D4221a2bFaE)



## Certora Analysis

### Proposal Types
{**TODO: Choose types from the following list.**}

* :gem: :new: Listing new assets

### Context
This publication proposes onboarding MetaMask's mUSD stablecoin to the Core instance of Aave v3 on Ethereum and Linea.
### Proposal Creation
Transaction: [0x00ee7c3ba284daeeb2ddd00dc273225678188abdd0aefceb4247fd6b4cb05b61](https://etherscan.io/tx/0x00ee7c3ba284daeeb2ddd00dc273225678188abdd0aefceb4247fd6b4cb05b61)
- `proposalId`: 415
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x49d30d20a4b529c3f9ff5834349e650169854b910c40b2070a929fa04d2b6dd6

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 374,
        },
        {
            chain: "59144",
            payloads_controller: "0x3BcE23a1363728091bc57A58a226CF2940C2e074",
            payload_id: 16,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x49d30d20a4b529c3f9ff5834349e650169854b910c40b2070a929fa04d2b6dd6",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/415.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/374.md)

* Linea - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/59144/0x3BcE23a1363728091bc57A58a226CF2940C2e074/16.md)


### Technical Analysis

The proposal is consistent with the description on both Snapshot and the governance forum.
We have validated consistency between the risk params.
We have verified token address and seed amounts with respect to decimal precision.
The payload logic, contract structure, configuration fields, and imports were checked against Aave V3 standards and static analysis plus execution simulation using Seatbelt confirmed correct behavior and no unexpected state changes.



### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.