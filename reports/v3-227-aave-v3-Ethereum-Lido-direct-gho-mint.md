# Proposal 227. Deploy 10M GHO into Aave v3 Lido Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=227)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-mint-deploy-10m-gho-into-aave-v3-lido-instance/19700)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x70E9fA954051a6B227249021A349Ae9e5aAD55Bf)



## Certora Analysis

### Proposal Types
* :moneybag: :receipt: Asset transfers
* :handshake: Permission granting and revoking

### Context
Due to demand of stablecoin borrows with LST collateral, and specifically wstETH-stable, the DAO sees value in bootstrapping an initial liquidity of Gho to the Lido specialized instance to provide risk buffer to gho liquidity providers.

### Proposal Creation
Transaction: [0x312eaf4ea70b4c2ae22b082832a71e689c00f3829b222026e43a22c746893074](https://etherscan.io/tx/0x312eaf4ea70b4c2ae22b082832a71e689c00f3829b222026e43a22c746893074)
- `proposalId`: 227
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x04c9882cee6c4dc847234ee6eef6bf81e75c1ded63ab00db2745012c602c2820

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 229,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0x04c9882cee6c4dc847234ee6eef6bf81e75c1ded63ab00db2745012c602c2820",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/227.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/229.md)


### Technical Analysis
1. The payload grants the `GhoDirectMinter` the necessary `risk_admin` role so the `GhoDirectMinter` will be able to change the gho supply cap as per the implementation strategy.

2. The payload also mints and supply 10M gho to the Lido instance.

3. The paylaod sets the `GhoDirectMinter` as a facilitator controlled by the `GhoBucketSteward`

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.