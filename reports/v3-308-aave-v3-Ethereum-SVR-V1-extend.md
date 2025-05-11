# Proposal 308. Extend SVR V1 to more reserves

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=308)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-aave-chainlink-svr-v1-activation-phase-2/21940)

### Payloads

* Ethereum core - [proposal payloads](https://etherscan.io/address/0x18f91eF698Fa11b7e09BB00aDd50b43f492Fa4D5)

* Ethereum prime - [proposal payloads](https://etherscan.io/address/0x7C133c6AA39fC5472d4A7B287D148F4d872AC6B8)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
Enable SVR feeds on the following assets:

- `eBTC`, `cbBTC` and `WBTC` on the Aave V3 Core instance
- `USDC`, `WETH`, `rsETH`, `ezETH` and `wstETH` on the Aave V3 Prime instance

### Proposal Creation
Transaction: [0xce5d2aeb4df11b8462313f6e4a7fbb54b0b43e93baf57d0550c8b72b24f0e114](https://etherscan.io/tx/0xce5d2aeb4df11b8462313f6e4a7fbb54b0b43e93baf57d0550c8b72b24f0e114)
- `proposalId`: 308
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0x03c2b1edc00d815c2ab96d2072d73620c011f691b028660f83e1cf969fef258f

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 283,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x03c2b1edc00d815c2ab96d2072d73620c011f691b028660f83e1cf969fef258f",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/308.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/283.md)

* Ethereum 2 - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/283.md)


### Technical Analysis
All the svr feeds have been validated to use the correct underlying and price feed source.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.