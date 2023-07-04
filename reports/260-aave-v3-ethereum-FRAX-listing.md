# Proposal 260. Aave v3 Ethereum - listing of FRAX

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=260](https://app.aave.com/governance/proposal/?proposalId=260)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-add-frax-to-aave-v3-ethereum/13051](https://governance.aave.com/t/arfc-add-frax-to-aave-v3-ethereum/13051)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists FRAX on the Aave v3 Ethereum pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x18d2fde474ea707c06b7e57895a9af2269b19ffeb58c305e2666c4925a3a3e7a](https://etherscan.io/tx/0x18d2fde474ea707c06b7e57895a9af2269b19ffeb58c305e2666c4925a3a3e7a)

```
- id: 260
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x56cf1dbd6cfca7898ba6a96ce1fbf1f038e6466b]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17595957
- endBlock: 17615157
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x9d5b0980afedbc2eda0e6106a8c6a1b7cbda2737b569c20588610aa12150625c
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/260.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/260.md)


<br>

### Technical analysis

The [proposal payload](https://etherscan.io/address/0x56cf1dbd6cfca7898ba6a96ce1fbf1f038e6466b#code#F1#L33) correctly uses the BGD's Aave Config Engine of Aave v3 Ethereum, in this case, its listing features.

We have verified this payload respects the interface required by the v3 config engine and effectively configures the FRAX listing with the following initial parameters:

- The asset is enabled for borrowing and the interest rate strategy is configured the following way:
  - Base variable borrow: 0%
  - Variable borrow slope 1: 4%
  - Variable borrow slope 2: 75%
  - Optimal point: 80%

- The asset is enabled as collateral in isolation
- LTV: 70%
- Liquidation Threshold: 75%
- Liquidation Bonus: 6%
- Liquidation Protocol Fee: 10%
- Reserve Factor: 10%
- Supply cap: 15'000'000 FRAX
- Borrow cap: 12'000'000 FRAX
- Debt ceiling: 10'000'000 USD
- No eMode category
- Flashlonable
- Not enabled for borrowing on isolation

The oracle used is a [Chainlink FRAX/USD](https://etherscan.io/address/0xB9E1E3A9feFf48998E45Fa90847ed4D467E8BcfD#readContract#F8).

The initial configuration is completely aligned with the [pre-approved by the community on Snapshot](https://snapshot.org/#/aave.eth/proposal/0xf0a3ef553905b03d36e0982719cfe25e85d97f563c3ef401f25e8455960576f8)


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
