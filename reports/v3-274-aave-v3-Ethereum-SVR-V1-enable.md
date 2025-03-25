# Proposal 274. Enable SVR V1 on Aave V3 Ethereum

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=274)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-aave-chainlink-svr-v1-phase-1-activation/21247)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x2Bf62876D711C97cc1EDaDB05e788429f8aA2010)


## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates

### Context
Activates SVR oracles on the AaveV3Ethereum instance for the assets LBTC, tBTC, LINK and AAVE.


### Proposal Creation
Transaction: [0xb6f3c327c86ba2881b91e55ada712e85946764a7dfbafc419df8d9e274fbdc37](https://etherscan.io/tx/0xb6f3c327c86ba2881b91e55ada712e85946764a7dfbafc419df8d9e274fbdc37)
- `proposalId`: 274
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x7942e73da2e2f7ece53e45370cdd9a9d8129a4eb7739959d2edb4828a7f95722

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 261,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0x7942e73da2e2f7ece53e45370cdd9a9d8129a4eb7739959d2edb4828a7f95722",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/274.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/261.md)


### Technical Analysis
We have verified that the correct SVR feeds are used (Through Chain Link website). We have verified the steward is changing the assets price feeds to the SVR price feeds.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.