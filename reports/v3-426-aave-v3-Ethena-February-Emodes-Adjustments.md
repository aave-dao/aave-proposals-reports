# Proposal 426. Ethena February E-Modes Adjustments

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=426)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-ethena-february-pts-caps-and-e-modes-adjustments/23501)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x00CeE4a3a05d8e82e55a9CBA5a48231456437ca4)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
This proposal is about adding sUSDe as an eligible collateral asset in both the PTsUSDe5FEB/Stablecoins and PTsUSDe5FEB/USDe E-Modes and USDe as an eligible collateral asset in both the PTUSDe5FEB/Stablecoins and PTUSDe5FEB/USDe E-Modes.


### Proposal Creation
Transaction: [0x899856b73a3425b4aa8f3a20d6ff5e960d77b8ece4b1f8c47a169b17d218a405](https://etherscan.io/tx/0x899856b73a3425b4aa8f3a20d6ff5e960d77b8ece4b1f8c47a169b17d218a405)
- `proposalId`: 426
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xde64c6c3b59d8a7ac29375e8bdab927b5cc5caf95929c12dfdb40d664486c1d3

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 383,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xde64c6c3b59d8a7ac29375e8bdab927b5cc5caf95929c12dfdb40d664486c1d3",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/426.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/383.md)


### Technical Analysis

We have confirmed alignment between the forum, IPFS, and the payload. 
We have checked the integrity of the imports. We have validated that `sUSDe` is set as collateral in both the `PTsUSDe5FEB/Stablecoins` and `PTsUSDe5FEB/USDe` E-Modes. We have validated that `USDe` is set as collateral in both the `PTUSDe5FEB/Stablecoins` and `PTUSDe5FEB/USDe` E-Modes. We have checked the payload's execution logic and verified it via Seatbelt.


The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.