# Proposal 259. Aave v3 Arbitrum - listing of FRAX

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=259](https://app.aave.com/governance/proposal/?proposalId=259)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-add-frax-arbitrum-aave-v3/13222](https://governance.aave.com/t/arfc-add-frax-arbitrum-aave-v3/13222)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists FRAX on the Aave v3 Arbitrum pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x95a8a8eabcebe48619de3d709d366a435f4f4327af43f671d4191bbccb0fedb0](https://etherscan.io/tx/0x95a8a8eabcebe48619de3d709d366a435f4f4327af43f671d4191bbccb0fedb0)

```
- id: 259
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xd1b3e25fd7c8ae7caddc6f71b461b79cd4ddcfa3]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000449e1b11bf74d57972d2d2cf057b337b203490c4]
- withDelegatecalls: [true]
- startBlock: 17595950
- endBlock: 17615150
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x94f29554f59f0d2c815511f891c540838808a46dca7d3f131b3ff9122e3551bd
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/259.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/259.md)

**Arbitrum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/259_Arbitrum_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/259_Arbitrum_pending_0.md)


<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Arbitrum.

The [proposal payload](https://arbiscan.io/address/0x449e1b11bf74d57972d2d2cf057b337b203490c4#code#F1#L32) correctly uses the BGD's Aave Config Engine of Aave v3 Arbitrum, in this case, its listing features.

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
- Supply cap: 7'000'000 FRAX
- Borrow cap: 5'500'000 FRAX
- Debt ceiling: 1'000'000 USD
- No eMode category
- Flashlonable
- Not enabled for borrowing on isolation

The oracle used is a [Chainlink FRAX/USD](https://arbiscan.io/address/0x0809e3d38d1b4214958faf06d8b1b1a2b73f2ab8#readContract#F8).

The initial configuration is completely aligned with the [pre-approved by the community on Snapshot](https://snapshot.org/#/aave.eth/proposal/0x03798dc3d6382f0d461590059d554a4405eefd5c95e3de917515702fdfc9ecfb)


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
