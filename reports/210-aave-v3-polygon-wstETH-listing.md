# Proposal 210. Aave v3 Polygon - listing of wstETH

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=210](https://app.aave.com/governance/proposal/?proposalId=210)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-add-support-for-wsteth-on-polygon-v3/12266](https://governance.aave.com/t/arc-add-support-for-wsteth-on-polygon-v3/12266)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists wstETH on the Aave v3 Polygon pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x81430b2467f3ba48a40a9118e22815814b936d35ce86e98f8860f6a842cfb745](https://etherscan.io/tx/0x81430b2467f3ba48a40a9118e22815814b936d35ce86e98f8860f6a842cfb745)

```
- id: 210
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000e11c89144259af51385f30b699cdb334d1e1dddc]
- withDelegatecalls: [true]
- startBlock: 17133313
- endBlock: 17152513
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x2e35445eb382526b009ad9175ad404ae5b010b29492ebe367592c0e9a2398563
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/210.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/210.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/210_fx_29_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/210_fx_29_0.md)


<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Polygon.

The [proposal payload](https://polygonscan.com/address/0xe11c89144259af51385f30b699cdb334d1e1dddc#code#F23#L1) correctly uses the new [BGD's Aave Config Engine of Aave v3 Polygon](https://polygonscan.com/address/0xe202f2fc4b6a37ba53cfd15be42a762a645fca07#code#F18#L1), in this case, its listing features.

We have verified this payload respects the interface required by the v3 config engine and effectively configures the wstETH asset with the following initial parameters:

- The asset is enabled for borrowing and the interest rate strategy follows the parameters on the forum:
  - Base variable borrow: 0.25%
  - Variable borrow slope 1: 4.5%
  - Variable borrow slope 2: 80%
  - Optimal point: 45%
- The asset is enabled as collateral with the following configuration:
  - LTV: 70%
  - Liquidation Threshold: 79%
  - Liquidation Bonus: 7.2%
  - Liquidation Protocol Fee: 10%
- Reserve Factor: 15%
- Supply cap: 1'800 wstETH
- Borrow cap: 285 wstETH
- e-mode category: ETH correlated (3)
- No isolation mode
- Not flashlonable
- Not enabled for borrowing on isolation

The oracle used is a BGD sync adapter [wstETH/ETH/USD](https://polygonscan.com/address/0xA2508729b1282Cc70dd33Ed311d4A9A37383035b#readContract#F6).

Additionally, the payload creates the ETH correlated new e-mode, adding to it both wstETH and WETH. This e-mode has the following configuration:
- ID: 3
- LTV: 90%
- Liquidation Threshold: 93%
- Liquidation Bonus: 1%

The initial configuration is completely aligned with the description on the Aave governance forum.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
