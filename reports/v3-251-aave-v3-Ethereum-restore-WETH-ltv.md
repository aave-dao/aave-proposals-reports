# Proposal 251. Prime Instance - Restore ETH LTV

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=251)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-prime-instance-restore-eth-ltv/20933)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x61D04C6146A07B87b4C6591bde6370bc477d0b87)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates

### Context
This publication proposes restoring ETH’s LTV to 82% on the Prime instance of Aave v3.

With the introduction of liquidity mining rewards for ETH deposits on Prime, some users exploited wETH/wETH leverage to farm rewards. In response, ETH’s LTV was set to 0, preventing new ETH collateral positions while preserving existing user positions.

Transitioning from direct liquidity mining emissions to a periodic Merkl distribution ensures that users leveraging wETH/wETH can be disqualified from rewards. By introducing a qualification criteria, incentives are directed towards users who engage with the protocol as intended.

This proposal focuses on re-enabling ETH collateral positions by restoring the LTV to 82%.

### Proposal Creation
Transaction: [0xf533c7fb3bb2c13efd7c50800270880a70e480ef3a2d9eac656fdaa0afbef476](https://etherscan.io/tx/0xf533c7fb3bb2c13efd7c50800270880a70e480ef3a2d9eac656fdaa0afbef476)
- `proposalId`: 251
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x0ae88db3b5a56cab72ad7bfded4baa1e46848e9fa4335cce2104c8c7876f6136

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 248,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0x0ae88db3b5a56cab72ad7bfded4baa1e46848e9fa4335cce2104c8c7876f6136",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/251.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/248.md)


### Technical Analysis
We have checked that the ltv is set to 82% and that the emode was configured to no in collateral for WETH

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.