# Proposal 273. Aave v3 Arbitrum - listing of ARB

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=273](https://app.aave.com/governance/proposal/?proposalId=273)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-add-arb-to-arbitrum-aave-v3/13225](https://governance.aave.com/t/arfc-add-arb-to-arbitrum-aave-v3/13225)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists ARB on the Aave v3 Arbitrum pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x9e4f34343afb717cfde993a4333e1ee7faa87e9e5accf637c01850fd8ef2dfea](https://etherscan.io/tx/0x9e4f34343afb717cfde993a4333e1ee7faa87e9e5accf637c01850fd8ef2dfea)

```
- id: 273
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xd1b3e25fd7c8ae7caddc6f71b461b79cd4ddcfa3]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000bf990c93a395f91ce769f2a4df78c0ddef038bc5]
- withDelegatecalls: [true]
- startBlock: 17684860
- endBlock: 17704060
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x5a1d09a98ce3bfe30f9584436d43dc11e220117ec05587283e93321ec49a3e7e
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/273.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/273.md)

**Arbitrum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/273_Arbitrum_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/273_Arbitrum_pending_0.md)


<br>

### Technical analysis

The [proposal payload](https://arbiscan.io/address/0xbf990c93a395f91ce769f2a4df78c0ddef038bc5#code#F1#L14) correctly uses the BGD's Aave Config Engine of Aave v3 Arbitrum, in this case, its listing features.

We have verified this payload respects the interface required by the v3 config engine and effectively configures the ARB listing with the following initial parameters:

- The asset is enabled for borrowing and the interest rate strategy is configured the following way:
  - Base variable borrow: 0%
  - Variable borrow slope 1: 7%
  - Variable borrow slope 2: 300%
  - Optimal point: 45%

- The asset is enabled as collateral in isolation
- LTV: 50%
- Liquidation Threshold: 60%
- Liquidation Bonus: 10%
- Liquidation Protocol fee: 10%
- Reserve Factor: 20%
- Supply cap: 20'000'000 ARB
- Borrow cap: 16'500'000 ARB
- Debt ceiling: 12'000'000 USD
- No eMode category
- Flashlonable
- Not enabled for borrowing on isolation

The oracle used is a [Chainlink ARB/USD](https://arbiscan.io/address/0xb2A824043730FE05F3DA2efaFa1CBbe83fa548D6#readContract#F8).

The initial configuration is completely aligned with the [pre-approved by the community on Snapshot](https://snapshot.org/#/aave.eth/proposal/0x308439517ffc8faa8709db0b4a1d131d2402ee8a3282cb79adf890de6135ec98)


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
