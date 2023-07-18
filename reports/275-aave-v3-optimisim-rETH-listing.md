# Proposal 275. Aave v3 Optimism - listing of rETH

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=275](https://app.aave.com/governance/proposal/?proposalId=275)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-add-reth-aave-v3-optimism/13795](https://governance.aave.com/t/arfc-add-reth-aave-v3-optimism/13795)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists rETH on the Aave v3 Optimism pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xe5f2066f49387b7deb1b7d0e9eae0b80a9cc3c2e68f26abfc568ee5d8dedb0ab](https://etherscan.io/tx/0xe5f2066f49387b7deb1b7d0e9eae0b80a9cc3c2e68f26abfc568ee5d8dedb0ab)

```
- id: 275
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000853844459106feefd8c7c4cc34066bfbc0531722]
- withDelegatecalls: [true]
- startBlock: 17693756
- endBlock: 17712956
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xf5cd680c7df66b2e603b4c16ffdb2c07e19903e6f4df9742886922d13000b839
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/275.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/275.md)

**Arbitrum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/275_Optimism_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/275_Optimism_pending_0.md)


<br>

### Technical analysis

The [proposal payload](https://optimistic.etherscan.io/address/0x853844459106feefd8c7c4cc34066bfbc0531722#code#F1#L15) correctly uses the BGD's Aave Config Engine of Aave v3 Optimism, in this case, its listing features.

We have verified this payload respects the interface required by the v3 config engine and effectively configures the rETH listing with the following initial parameters:

- The asset is enabled for borrowing and the interest rate strategy is configured the following way:
  - Base variable borrow: 0%
  - Variable borrow slope 1: 7%
  - Variable borrow slope 2: 300%
  - Optimal point: 45%

- The asset is enabled as collateral
- LTV: 67%
- Liquidation Threshold: 74%
- Liquidation Bonus: 7.5%
- Liquidation Protocol fee: 10%
- Reserve Factor: 15%
- Supply cap: 6'000 rETH
- Borrow cap: 720 rETH
- eMode category: ETH-correlated
- Flashlonable
- Not enabled for borrowing on isolation

The oracle used is a BGD CL Synchronicity price adapter [rETH/ETH/USD](https://optimistic.etherscan.io/address/0x52d5F9f884CA21C27E2100735d793C6771eAB793#readContract#F8).

The initial configuration is completely aligned with the [pre-approved by the community on Snapshot](https://snapshot.org/#/aave.eth/proposal/0xb112684943ef900f2918ccbc4de3bb3091869eaeb6b3c15cc26805c17cb6a9f6)


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
