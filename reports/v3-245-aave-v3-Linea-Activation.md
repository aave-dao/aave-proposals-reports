# Proposal 245. Aave v3 Linea Activation

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=245)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-deployment-of-aave-on-linea/19852/6)

### Payloads

* Linea - [proposal payloads](https://lineascan.build//0xC89595903010eef079CAE8050ad0166B1DB5B144)


## Certora Analysis

### Proposal Types
* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates
* :gem: :new: Listing new assets

### Context
This proposal allows the Aave governance to activate the Aave V3 Linea pool (3.2) by completing all the initial setup and listing USDC, USDT, WETH, WBTC, wstETH, ezETH, weETH as suggested by the risk service providers engaged with the DAO on the governance [forum](https://governance.aave.com/t/arfc-deployment-of-aave-on-linea/19852/6#p-50536-specification-10).

All the Aave Linea V3 addresses can be found in the [aave-address-book](https://github.com/bgd-labs/aave-address-book/blob/837214a8bfff3c937a6d8fd803d0c88eeaa948a0/src/AaveV3Linea.sol).

### Proposal Creation
Transaction: [0x62b5a946b2e8d2ca58122acabfb075ce77be27f669f5dd3937dd8e243ac00807](https://etherscan.io/tx/0x62b5a946b2e8d2ca58122acabfb075ce77be27f669f5dd3937dd8e243ac00807)
- `proposalId`: 245
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0xa6934c5bd7d57c2bff6c7f996ebc6723ab4c6cba58e2c1ce82e18220ad75a560

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "59144",
            payloads_controller: "0x3BcE23a1363728091bc57A58a226CF2940C2e074",
            payload_id: 3,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0xa6934c5bd7d57c2bff6c7f996ebc6723ab4c6cba58e2c1ce82e18220ad75a560",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/245.md)

**Payload Reports**

* Linea - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/59144/0x3BcE23a1363728091bc57A58a226CF2940C2e074/3.md)


### Technical Analysis
We have verified the specified parameters for each listed asset are correct. We have validated the price feed correctness. We checked the amounts of the SEED_AMOUNT of each asset are correct and supplied to the pool.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.