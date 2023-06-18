# Proposal 242. Aave v3 Arbitrum - listing of rETH

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=242](https://app.aave.com/governance/proposal/?proposalId=242)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-add-reth-to-aave-v3-arbitrum-liquidity-pool/12810](https://governance.aave.com/t/arfc-add-reth-to-aave-v3-arbitrum-liquidity-pool/12810)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists rETH (Rocket Pool ETH) on the Aave v3 Arbitrum pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x537bb6755c9d8b4f4e7c73a7fcd266466a331767030051c25430af687d81cc7e](https://etherscan.io/tx/0x537bb6755c9d8b4f4e7c73a7fcd266466a331767030051c25430af687d81cc7e)

```
- id: 242
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xd1b3e25fd7c8ae7caddc6f71b461b79cd4ddcfa3]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x00000000000000000000000015066c53340cd87480e3a33046a77edd4063984f]
- withDelegatecalls: [true]
- startBlock: 17474258
- endBlock: 17493458
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x8d4f6f42043d8db567d5e733762bb84a6f507997a779a66b2d17fdf9de403c13
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/242.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/242.md)

**Arbitrum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/242_Arbitrum_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/242_Arbitrum_pending_0.md)


<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Arbitrum.

The [proposal payload](https://arbiscan.io/address/0x15066c53340cd87480e3a33046a77edd4063984f#code) correctly uses the BGD's Aave Config Engine of Aave v3 Arbitrum, in this case, its listing features.

We have verified this payload respects the interface required by the v3 config engine and effectively configures the rETH listing with the following initial parameters:

- The asset is enabled for borrowing and the interest rate strategy follows the parameters on the forum:
  - Base variable borrow: 0%
  - Variable borrow slope 1: 7%
  - Variable borrow slope 2: 300%
  - Optimal point: 45%

- The asset is enabled as collateral
- LTV: 67%
- Liquidation Threshold: 74%
- Liquidation Bonus: 7.5%
- Liquidation Protocol Fee: 10%
- Reserve Factor: 15%
- Supply cap: 325 rETH
- Borrow cap: 85 rETH
- No eMode category
- Flashlonable
- Not enabled for borrowing on isolation

The oracle used is a [BGD Price Sync Adapter](https://arbiscan.io/address/0x04c28D6fE897859153eA753f986cc249Bf064f71#readContract#F8) with the following components:
- [rETH/ETH exchange rate feed](https://arbiscan.io/address/0xf3272cafe65b190e76caaf483db13424a3e23dd2#readContract#F8)
- [ETH/USD](https://arbiscan.io/address/0x639fe6ab55c921f74e7fac1ee960c0b6293ba612#readContract#F8)

The initial configuration is completely aligned with the description on the Aave governance forum.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
