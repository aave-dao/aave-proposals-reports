# Proposal 461. Enable SVR on Base and Arbitrum

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=461)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-aave-chainlink-svr-multi-network-expansion-base-arbitrum/24241)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x4CD5a066d8932e47604A52bD5D2821bAB1dc3EB6)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0xfd3a8b0A0a6B1dB39e4F63C98C1d6C97Bb2D2599)

* Base - [proposal payloads](https://basescan.org/address/0x43Ead112F72D8d7f7301707A0d5a5e681E19a75f)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates


### Context

After a successful implementation of SVR on Ethereum, we aim to expand its coverage to Base and Arbitrum networks.

### Proposal Creation
Transaction: [0xfce6c761b1628a23d24731ab515e85edfd2ec52836c90816f6a490f9676ad293](https://etherscan.io/tx/0xfce6c761b1628a23d24731ab515e85edfd2ec52836c90816f6a490f9676ad293)
- `proposalId`: 461
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0xf1fd379d3fbcc5854c8981f4029968ee35b9eb6e891c3bdd741badd489ca3a68

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 419,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 115,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 102,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xf1fd379d3fbcc5854c8981f4029968ee35b9eb6e891c3bdd741badd489ca3a68",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/461.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/419.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/115.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/102.md)


### Technical Analysis
We confirmed the registration of the new SVR oracles on the `SvrOracleSteward` contracts via the `enableSvrOracles()` calls.

We verified that the `AaveOracle` is accurately configured to enforce the new SVR price feeds for 17 assets on Arbitrum and 14 on Base, aligning these networks with the Ethereum mainnet.

We confirmed the assignment of the `ASSET_LISTING_ADMIN_ROLE` role to the `SvrOracleSteward` contracts.

We have verified proposal logic and validate its execution via seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.