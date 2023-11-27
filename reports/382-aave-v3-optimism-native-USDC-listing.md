# Proposal 382. Aave v3 Optimism - listing of native USDC

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=382](https://app.aave.com/governance/proposal/?proposalId=382)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-onboard-native-usdc-to-aave-v3-optimism-market/15463](https://governance.aave.com/t/arfc-onboard-native-usdc-to-aave-v3-optimism-market/15463)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

:wrench: :bar_chart: params-update

<br>

### Context

This proposal lists native USDC (USDC coin) on the Aave v3 Optimism pool. Additionally, it also updates certain configurations (RF, caps) for USDC.e.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xd6dab3de4dc8d3122f85df96490affce1477f24875818769567eec90cd6ba255](https://etherscan.io/tx/0xd6dab3de4dc8d3122f85df96490affce1477f24875818769567eec90cd6ba255)

```
- id: 382
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x000000000000000000000000000000000000000000000000000000000000000a00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000e1a3af1f9cc76a62ed31ededca291e63632e7c40000000000000000000000000000000000000000000000000000000000000005]
- withDelegatecalls: [false]
- startBlock: 18636679
- endBlock: 18655879
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x1a6c69fcf8d44afae186c84ef32a80cd702a75951a60f9069e2b9adb311d8349
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/382.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/382.md)


**Payload report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/5.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/5.md)


<br>

### Technical analysis

The [proposal payload](https://optimistic.etherscan.io/address/0x41DaCfA8Bc41221F46c780fD6469dAD4CDCceF83#code#F1#L18) correctly uses the BGD's Aave Config Engine of Aave v3 Optimism, in this case, its listing features.

We have verified this payload respects the interface required by the v3 config engine and effectively configures the native USDC listing with the following initial parameters:

- The asset is enabled for borrowing and the interest rate strategy is configured the following way:
  - Base variable borrow: 0%
  - Variable borrow slope 1: 3.5%
  - Variable borrow slope 2: 60%
  - Optimal point: 90%

- The asset is enabled as collateral
- LTV: 80%
- Liquidation Threshold: 85%
- Liquidation Bonus: 50%
- Liquidation Protocol fee: 10%
- Reserve Factor: 10%
- Supply cap: 25'000'000 USDC
- Borrow cap: 20'000'000 USDC
- Stablecoins eMode category
- Flashlonable
- Enabled for borrowing on isolation

The oracle used is a [Chainlink USDC/USD](https://optimistic.etherscan.io/address/0x16a9FA2FDa030272Ce99B29CF780dFA30361E0f3#readContract#F8).

<br>

---

<br>

Additionally, the following changes are applied to USDC.e (non-native):

- Supply cap: 150'000'000 USDC.e -> **25'000'000 USDC.e**
- Borrow cap: 100'000'000 USDC.e -> **20'000'000 USDC.e**
- Reserve factor: 10% -> **20%**

<br>

The initial configuration is completely aligned with the the Aave governance forum and Snapshot.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
