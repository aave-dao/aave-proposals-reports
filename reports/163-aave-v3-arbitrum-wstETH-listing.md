# Proposal 163. Aave v3 Arbitrum - listing of wstETH

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=163](https://app.aave.com/governance/proposal/?proposalId=163)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-add-support-for-wsteth-on-arbitrum-aave-v3/11387](https://governance.aave.com/t/arc-add-support-for-wsteth-on-arbitrum-aave-v3/11387)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists wstETH (wrapped stETH) on the Aave v3 Arbitrum pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xb911b6fe869c33b97f9444ebeb900d50afe0bfb8c0b656444edeb8c415cadaac](https://etherscan.io/tx/0xb911b6fe869c33b97f9444ebeb900d50afe0bfb8c0b656444edeb8c415cadaac)

```
- id: 163
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x2e2b1f112c4d79a9d22464f0d345de9b792705f1]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x00000000000000000000000080cb7e9e015c5331bf34e06de62443d070fd6654]
- withDelegatecalls: [true]
- startBlock: 16686653
- endBlock: 16705853
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xfbf20135455b8d70030cfb114c1eee75368d96bce0e76b749c1372942b2bbcb5
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/163.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/163.md)

**Arbitrum**

Aave Seatbelt doesn't support Arbitrum yet.

<br>

### Technical analysis

The [proposal payload](https://arbiscan.io/address/0x80cb7e9e015c5331bf34e06de62443d070fd6654#code#F18#L1) follows the new approach for listings, using the [Aave V3 listing engine contract](https://arbiscan.io/address/0x7b8Fa4540246554e77FCFf140f9114de00F8bB8D#code), containing logic to expose a simple interface, and do proper validations.

We have verified this payload respects the interface required by the v3 listing engine and effectively configures the wstETH listing with the following initial parameters:

- The asset is enabled for borrowing and the interest rate strategy follows the parameters on the forum:
  - Base variable borrow: 0.25%
  - Variable borrow slope 1: 4.5%
  - Variable borrow slope 2: 80%
  - Optimal point: 45%
- LTV: 70%
- Liquidation Threshold: 79%
- Liquidation Bonus: 7.2%
- Reserve Factor: 15%
- Liquidation protocol fee: 10%
- Supply cap: 1'200 wstETH
- Borrow cap: 190 wstETH
- 2, ETH-correlated assets
- No isolation mode
- Flashloanable (Aave v3 Optimism doesn't have 3.0.1 yet, so all assets listed are flashloanable).
- Not enabled for borrowing on isolation

The oracle used is [price sync adapter wstETH/stETH/USD](https://arbiscan.io/address/0x230E0321Cf38F09e247e50Afc7801EA2351fe56F#readContract#F6).

The initial configuration is completely aligned with the description on the Aave governance forum.

<br>

Additionally, the payload creates the new ETH-correlated eMode with the following specifications:
- LTV: 90%
- Liquidation Threshold: 93%
- Liquidation Bonus: 2%

To be consistent with the intention of the proposal, WETH gets introduced into the new eMode too.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
