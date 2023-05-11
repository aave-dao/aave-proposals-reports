# Proposal 218. Aave v3 Optimism - listing of MAI

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=218](https://app.aave.com/governance/proposal/?proposalId=218)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-add-mai-to-optimism-aave-v3-pool/12765](https://governance.aave.com/t/arfc-add-mai-to-optimism-aave-v3-pool/12765)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists MAI on the Aave v3 Optimism pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xec489ad15bdeb1cd478b517249f403b3e4d5142bf7c3f10fdfed91f6cadfaad1](https://etherscan.io/tx/0xec489ad15bdeb1cd478b517249f403b3e4d5142bf7c3f10fdfed91f6cadfaad1)

```
- id: 218
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x0000000000000000000000001720d605289a189c5fbd360ca2307db5c6d3fdfd]
- withDelegatecalls: [true]
- startBlock: 17223447
- endBlock: 17242647
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x4a52c673dc62b4e293c3c3a2d37aace4c567bcfba3de640d1e89b5ed008a284a
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/218.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/218.md)

**Optimism**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/218_optimism_15_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/218_optimism_15_0.md)


<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Optimism.

The [proposal payload](https://optimistic.etherscan.io/address/0x1720d605289a189c5fbd360ca2307db5c6d3fdfd#code#F22#L16) correctly uses the [BGD's Aave Config Engine of Aave v3 Optimism](https://optimistic.etherscan.io/address/0x7a9a9c14b35e58ffa1cc84ab421ace0fdcd289e3#code#F18#L1), in this case, its listing features.

We have verified the payload respects the interface required by the v3 config engine and lists the MAI asset with the following configurations:

<br>

**MAI**

- The asset is enabled for borrowing and the interest rate strategy follows the parameters on Snapshot:
  - Base variable borrow: 0%
  - Variable borrow slope 1: 4%
  - Variable borrow slope 2: 75%
  - Optimal point: 80%
- The asset is enabled as collateral in isolation
- LTV: 75%
- Liquidation Threshold: 80%
- Liquidation Bonus: 5%
- Liquidation Protocol Fee: 10%
- Reserve Factor: 20%
- Supply cap: 7'600'000 MAI
- Borrow cap: 2'500'000 MAI
- Debt ceiling 1'900'000 USD
- No eMode category
- Not flashlonable
- Not enabled for borrowing on isolation

The oracle used is a [Chainlink MAI/USD feed](https://optimistic.etherscan.io/address/0x73A3919a69eFCd5b19df8348c6740bB1446F5ed0#readContract#F8).

The initial configuration is completely aligned with the [recommendations of risk providers in the Aave governance forum](https://governance.aave.com/t/arfc-add-mai-to-optimism-aave-v3-pool/12765/5).


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
