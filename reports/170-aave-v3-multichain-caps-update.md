# Proposal 170. Aave v3 Polygon, Optimism, Arbitrum - update of supply/borrow caps

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=170](https://app.aave.com/governance/proposal/?proposalId=170)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-chaos-labs-supply-and-borrow-cap-updates-aave-v3-2023-02-24/12048](https://governance.aave.com/t/arc-chaos-labs-supply-and-borrow-cap-updates-aave-v3-2023-02-24/12048)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates multiple supply and borrow caps on Aave v3 Polygon, Optimism and Arbitrum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x64b62a9c4add64c76b7dda4138e9f3ea51de907475044fbe7c9e92763fdcc659](https://etherscan.io/tx/0x64b62a9c4add64c76b7dda4138e9f3ea51de907475044fbe7c9e92763fdcc659)

```
- id: 170
- creator: 0xbc540e0729b732fb14afa240aa5a047ae9ba7df0
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b,0x2e2b1f112c4d79a9d22464f0d345de9b792705f1,0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711]
- values: [0,0,0]
- signatures: [execute(address),execute(address),execute(address)]
- calldatas: [0x000000000000000000000000eca5bdf0c2b352cbe2d9a19b555e1ec269d4765c,0x000000000000000000000000060bea15af594fe9e0a243ca632f2c7d1935c70f,0x0000000000000000000000003a4f2a6c7e1e641afad6300553a0bb82d6c46a2e]
- withDelegatecalls: [true,true,true]
- startBlock: 16777322
- endBlock: 16796522
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x435d26048b2f67302c898a9f0049e4d3a16bfa3d71c8bef63f7c60ce78db732c
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/170.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/170.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/170_fx_17_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/170_fx_17_0.md)

**Optimism**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/170_optimism_7_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/170_optimism_7_0.md)


**Arbitrum**

Aave Seatbelt doesn't support Arbitrum yet.

<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Polygon, Optimism and Arbitrum.
The proposals payloads do the following:

**[Polygon](https://polygonscan.com/address/0xeca5bdf0c2b352cbe2d9a19b555e1ec269d4765c#code#F15#L1)**

By calling the [PoolConfigurator of Aave v3 Polygon](https://polygonscan.com/address/0x8145eddDf43f50276641b55bd3AD95944510021E) it changes the following caps:

- WETH supply cap: 26'900 WETH -> **50'000 WETH**
- AAVE supply cap: 36'820 AAVE -> **70'000 AAVE**

<br>

**[Optimism](https://optimistic.etherscan.io/address/0x3a4f2a6c7e1e641afad6300553a0bb82d6c46a2e#code#F15#L1)**

By calling the [PoolConfigurator of Aave v3 Optimism](https://optimistic.etherscan.io/address/0x8145eddDf43f50276641b55bd3AD95944510021E) it changes the following caps:

- DAI supply cap: 2'000'000'000 DAI -> **25'000'000 DAI**
- DAI borrow cap: No cap -> **16'000'000 DAI**
- sUSD borrow cap: No cap -> **13'000'000 sUSD**
- USDC supply cap: 2'000'000'000 USDC -> **150'000'000 USDC**
- USDC borrow cap: No cap -> **100'000'000 USDC**
- USDT supply cap: 2'000'000'000 USDT -> **25'000'000 USDT**
- USDT borrow cap: No cap -> **16'000'000 USDT**
- AAVE supply cap: 100'000 AAVE -> **45'000 AAVE**
- LINK supply cap: 258'000 LINK -> **160'000 LINK**
- LINK borrow cap: 141'900 LINK -> **84'000 LINK**
- WBTC supply cap: 1'100 WBTC -> **620 WBTC**
- WBTC borrow cap: 605 WBTC -> **250 WBTC**

<br>

**[Arbitrum](https://arbiscan.io/address/0x060bea15af594fe9e0a243ca632f2c7d1935c70f#code#F15#L1)**

By calling the [PoolConfigurator of Aave v3 Arbitrum](https://arbiscan.io/address/0x8145eddDf43f50276641b55bd3AD95944510021E) it changes the following caps:

- DAI supply cap: 2'000'000'000 DAI -> **50'000'000 DAI**
- DAI borrow cap: No cap -> **30'000'000 DAI**
- EURS supply cap: No cap -> **60'000 EURS**
- EURS borrow cap: No cap -> **45'000 EURS**
- USDC supply cap: 2'000'000'000 USDC -> **150'000'000 USDC**
- USDC borrow cap: No cap -> **100'000'000 USDC**
- USDT supply cap: 2'000'000'000 USDT -> **50'000'000 USDT**
- USDT borrow cap: No cap -> **35'000'000 USDT**
- AAVE supply cap: 2'500 AAVE -> **1'850 AAVE**


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
