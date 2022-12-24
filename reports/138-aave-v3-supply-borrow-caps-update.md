# Proposal 138. Aave v3 - Supply/borrow caps update on Polygon, Optimism and Arbitrum

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=138](https://app.aave.com/governance/proposal/?proposalId=138)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-v3-borrow-cap-recommendations-fast-track-2022-12-05/10927](https://governance.aave.com/t/arc-v3-borrow-cap-recommendations-fast-track-2022-12-05/10927)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal is an update of supply and borrow caps affecting Aave v3 Polygon/Optimism and Arbitrum, by Chaos Labs.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x655d3b3f0ad7894e6574a5723c37dd3022ac3ff7fea3895b5d2faad64a6443bf](https://etherscan.io/tx/0x655d3b3f0ad7894e6574a5723c37dd3022ac3ff7fea3895b5d2faad64a6443bf)

```
- id: 138
- creator: 0xbc540e0729b732fb14afa240aa5a047ae9ba7df0
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711,0x2e2b1f112c4d79a9d22464f0d345de9b792705f1,0x158a6bc04f0828318821bae797f50b0a1299d45b,0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711,0x2e2b1f112c4d79a9d22464f0d345de9b792705f1]
- values: [0,0,0,0,0]
- signatures: [execute(address),execute(address),execute(address),execute(address),execute(address)]
- calldatas: [0x000000000000000000000000280e404338d9d8e50b11d6677b9c91ba86e0fd22,0x000000000000000000000000691b41805f7ef2d7de6165bc42295b035a31600d,0x000000000000000000000000691b41805f7ef2d7de6165bc42295b035a31600d,0x000000000000000000000000691b41805f7ef2d7de6165bc42295b035a31600d,0x000000000000000000000000c9df68edcb0c8fb7ced82e5836b75c002c723e17]
- withDelegatecalls: [true,true,true,true,true]
- startBlock: 16235428
- endBlock: 16254628
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x366f499db7fed9b542e614e587312e417b6d8add2fc83840745781f5a70567b1
```

<br>

### Aave Seatbelt reports

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/138.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/138.md)


**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/138_fx_9_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/138_fx_9_0.md)

**Optimism**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/138_optimism_0_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/138_optimism_0_0.md)

We have noticed a problem with the second report of Optimism (supply caps), but we can confirm the payload is correct.


**Arbitrum**

Aave Seatbelt doesn't support Arbitrum yet.


<br>

### Technical analysis

From a technical perspective, we have verified that the proposal payload does the following changes on Polygon, Optimism and Arbitrum:

1. Polygon:
  - CRV borrow cap changed to **640'437 CRV**
  - WBTC borrow cap changed to **851 WBTC**
  - GHST borrow cap changed to **3'234'000 GHST**
  - LINK borrow cap changed to **163'702 LINK**
  - WETH borrow cap changed dto **14'795 WETH**
  - DPI borrow cap changed to **779 DPI**
  - BAL borrow cap changed to **156'530 BAL**

2. Optimism
  - LINK borrow cap changed to **141'900 LINK**
  - WETH borrow cap changed to **19'745 WETH**
  - WBTC borrow cap changed to **605 WBTC**
  - LINK supply cap changed to **258'000 LINK**
  - WETH supply cap changed to **35'900 WETH**
  - WBTC supply cap changed to **1'100 WBTC**

3. Arbitrum
  - LINK borrow cap changed to **242'249 LINK**
  - WETH borrow cap changed to **11'165 WETH**
  - WBTC borrow cap changed to **1'115 WBTC**
  - LINK supply cap changed to **350'000 LINK**
  - WETH supply cap changed to **20'300 WETH**
  - WBTC supply cap changed to **2'100 WBTC**
  - AAVE supply cap changed to **2'500 AAVE**

We have only noticed a inconsistency on the borrow cap of WBTC on Arbitrum, being 1'115 WBTC on the payload compared with 1'155 WBTC on the AIP description. Given that the one to be applied in the payload is even more conservative and relatively close, we don't see it as a meaningful problem.



<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
