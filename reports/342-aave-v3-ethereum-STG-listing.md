# Proposal 342. Aave v3 Ethereum - listing of STG

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=342](https://app.aave.com/governance/proposal/?proposalId=342)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-stg-onboarding-on-aavev3-ethereum-market/14973](https://governance.aave.com/t/arfc-stg-onboarding-on-aavev3-ethereum-market/14973)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists STG (StargateToken) on the Aave v3 Ethereum pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x5fd8bd389f5096bacdfe73cac118550dbc3d420a1cd025869921fbe432732d05](https://etherscan.io/tx/0x5fd8bd389f5096bacdfe73cac118550dbc3d420a1cd025869921fbe432732d05)

```
- id: 342
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x4e7d1afac9af73fc96ae4382dbffc7dd358a6568]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 18333261
- endBlock: 18352461
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x314df0c789153ce4a76dbfa5ef93b397bf75b8aa307dae3f4bf287a9f6d7526f
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/342.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/342.md)


<br>

### Technical analysis

The [proposal payload](https://etherscan.io/address/0x4e7d1afac9af73fc96ae4382dbffc7dd358a6568#code#F1#L12) correctly uses the BGD's Aave Config Engine of Aave v3 Ethereum, in this case, its listing features.

We have verified this payload respects the interface required by the v3 config engine and effectively configures the STG listing with the following initial parameters:

- The asset is enabled for borrowing and the interest rate strategy is configured the following way:
  - Base variable borrow: 0%
  - Variable borrow slope 1: 7%
  - Variable borrow slope 2: 300%
  - Optimal point: 45%

- The asset is enabled as collateral in isolation
- LTV: 35%
- Liquidation Threshold: 40%
- Liquidation Bonus: 10%
- Liquidation Protocol fee: 10%
- Reserve Factor: 20%
- Supply cap: 10'000'000 STG
- Borrow cap: 5'500'000 STG
- Debt ceiling: 3'000'000 USD
- No eMode category
- Flashlonable
- Not enabled for borrowing on isolation

The oracle used is a [Chainlink STG/USD](https://etherscan.io/address/0x7A9f34a0Aa917D438e9b6E630067062B7F8f6f3d#readContract#F8).

The initial configuration is completely aligned with the [pre-approved by the community on Snapshot](https://signal.aave.com/#/proposal/0x917d0a2c0d9a107d5f8c83b76c291bb34a6a94b85b833b2add96bce7681522ef)


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
