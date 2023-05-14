# Proposal 217. Aave v3 Ethereum, Polygon, Arbitrum, Optimism - Caps update

<br>


### Voting link

[https://app.aave.com/governance/proposal/?proposalId=217](https://app.aave.com/governance/proposal/?proposalId=217)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-supply-and-borrow-cap-updates-04-21-2023/12845](https://governance.aave.com/t/arfc-chaos-labs-supply-and-borrow-cap-updates-04-21-2023/12845)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates supply and borrow caps of multiple assets across Aave v3 Ethereum, Polygon, Optimism and Arbitrum.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x3a12805b0ef362039a98eceab1de64ceba9b3cf0819a2a2711ac84d9bf9c376a](https://etherscan.io/tx/0x3a12805b0ef362039a98eceab1de64ceba9b3cf0819a2a2711ac84d9bf9c376a)

```
- id: 217
- creator: 0xbc540e0729b732fb14afa240aa5a047ae9ba7df0
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b,0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711,0xd1b3e25fd7c8ae7caddc6f71b461b79cd4ddcfa3,0x8070dd4aee19048581d61543adecfa3dd7f165c1]
- values: [0,0,0,0]
- signatures: [execute(address),execute(address),execute(address),execute()]
- calldatas: [0x000000000000000000000000ac9ae3591c784275f452b5b9f7121a9122dc8bfe,0x000000000000000000000000050997fc08733eb8593c04102706d8d2e7a9443e,0x000000000000000000000000c53586aa2626094bd33c123794e34417ea877a36,0x]
- withDelegatecalls: [true,true,true,true]
- startBlock: 17194185
- endBlock: 17213385
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x145c5e5f8f1806f069ad9eb41d0a6e8f15c6e04877102249785ebd0fd6caeb98
```

<br>

### Aave Seatbelt reports

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/217.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/217.md)


**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/217_fx_35_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/217_fx_35_0.md)

**Optimism**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/217_optimism_15_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/217_optimism_15_0.md)

**Arbitrum**

Aave Seatbelt doesn't support Arbitrum yet.


<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system in the parts communicating with Polygon, Optimism and Arbitrum.

Regarding each payload, the changes applied are the following:

**[Ethereum](https://etherscan.io/address/0x8070dd4aee19048581d61543adecfa3dd7f165c1#code#F22#L1)**

- wstETH:
  - Borrow cap: 6'000 wstETH -> **12'000 wstETH**

**[Polygon](https://polygonscan.com/address/0xac9ae3591c784275f452b5b9f7121a9122dc8bfe#code#F22#L1)**

- WBTC:
  - Supply cap: 1'548 WBTC -> **3'100 WBTC**

- LINK:
  - Supply cap: 297'640 LINK -> **370'000 LINK**

**[Optimism](https://optimistic.etherscan.io/address/0x050997fc08733eb8593c04102706d8d2e7a9443e#code#F22#L1)**

- WBTC:
  - Supply cap: 620 WBTC -> **1'200 WBTC**

- wstETH:
  - Supply cap: 6'000 wstETH -> **12'000 wstETH**

**[Arbitrum](https://arbiscan.io/address/0xc53586aa2626094bd33c123794e34417ea877a36#code#F22#L1)**

- WBTC:
  - Supply cap: 2'100 WBTC -> **4'200 WBTC** 

- WETH:
  - Supply cap: 45'000 WETH -> **70'000 WETH**
  - Borrow cap: 11'165 WETH -> **20'000 WETH**


<br>

The caps updates are aligned with those defined in the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
