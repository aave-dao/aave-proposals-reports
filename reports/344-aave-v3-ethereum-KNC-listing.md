# Proposal 344. Aave v3 Ethereum - listing of KNC

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=344](https://app.aave.com/governance/proposal/?proposalId=344)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-knc-onboarding-on-aavev3-ethereum-market/14972](https://governance.aave.com/t/arfc-knc-onboarding-on-aavev3-ethereum-market/14972)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists KNC (Kyber Network Crystal v2) on the Aave v3 Ethereum pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x30f6426e4058805758d9dc270650f73a55a25b930b76d4f0a222ec17f7965af1](https://etherscan.io/tx/0x30f6426e4058805758d9dc270650f73a55a25b930b76d4f0a222ec17f7965af1)

```
- id: 344
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x29ba7784ab57db44c51ccd3743aa2b792f8523ac]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 18340369
- endBlock: 18359569
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xf898a288827ec9ea9ce851d67937658a85221a87d534ae0ca730f072c66d268f
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/344.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/344.md)


<br>

### Technical analysis

The [proposal payload](https://etherscan.io/address/0x29ba7784ab57db44c51ccd3743aa2b792f8523ac#code#F1#L12) correctly uses the BGD's Aave Config Engine of Aave v3 Ethereum, in this case, its listing features.

We have verified this payload respects the interface required by the v3 config engine and effectively configures the KNC listing with the following initial parameters:

- The asset is enabled for borrowing and the interest rate strategy is configured the following way:
  - Base variable borrow: 0%
  - Variable borrow slope 1: 9%
  - Variable borrow slope 2: 300%
  - Optimal point: 45%

- The asset is enabled as collateral in isolation
- LTV: 35%
- Liquidation Threshold: 40%
- Liquidation Bonus: 10%
- Liquidation Protocol fee: 10%
- Reserve Factor: 20%
- Supply cap: 1'200'000 KNC
- Borrow cap: 650'000 KNC
- Debt ceiling: 1'000'000 USD
- No eMode category
- Flashlonable
- Not enabled for borrowing on isolation

The oracle used is a [Chainlink KNC/USD](https://etherscan.io/address/0xf8fF43E991A81e6eC886a3D281A2C6cC19aE70Fc#readContract#F8).

The initial configuration is completely aligned with the [pre-approved by the community on Snapshot](https://snapshot.org/#/aave.eth/proposal/0xa162335479f27fe1bf4482da63e1f6fa246b0fd770d913d8ba89bd56a5aa644f)


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
