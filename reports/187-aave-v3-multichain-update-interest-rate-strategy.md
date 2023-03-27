# Proposal 187. Aave v3 Polygon, Optimism and Arbitrum - update rate strategies

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=187](https://app.aave.com/governance/proposal/?proposalId=187)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-gauntlet-interest-rate-curve-changes-for-aave-v3-markets-feb-2023/11851/3](https://governance.aave.com/t/arc-gauntlet-interest-rate-curve-changes-for-aave-v3-markets-feb-2023/11851/3)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the interest rate strategies for multiple assets on Aave v3 Polygon, Optimism and Arbitrum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xb96cb8d95012c6f271057b4966f35fe4c87198ae3284df52ce5da0bb848599a4](https://etherscan.io/tx/0xb96cb8d95012c6f271057b4966f35fe4c87198ae3284df52ce5da0bb848599a4)

```
- id: 187
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b,0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711,0x2e2b1f112c4d79a9d22464f0d345de9b792705f1]
- values: [0,0,0]
- signatures: [execute(address),execute(address),execute(address)]
- calldatas: [0x000000000000000000000000dbe6eb920ca5a79ae2151b6dcbd2c1fa3a19ad1a,0x0000000000000000000000007902f3c60f05b5a6b7e4ce0cac11cb17bc8e607c,0x0000000000000000000000007a9a9c14b35e58ffa1cc84ab421ace0fdcd289e3]
- withDelegatecalls: [true,true,true]
- startBlock: 16880458
- endBlock: 16899658
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x3b66ed0fa57bec842608cb1be68f97ca0c241cd3744a860086762f76cc0ae933
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/187.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/187.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/187_fx_22_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/187_fx_22_0.md)

**Optimism**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/187_optimism_8_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/187_optimism_8_0.md)

**Arbitrum**

Aave Seatbelt doesn't support Arbitrum yet.

<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Polygon, Optimism and Arbitrum.
The proposals payloads do the following:

**[Polygon](https://polygonscan.com/address/0xdbe6eb920ca5a79ae2151b6dcbd2c1fa3a19ad1a#code#F21#L1)**

On Aave v3 Polygon, the proposal payload includes 2 types of updates:

_Reserve Factors_

- GHST: 20% -> **35%**
- WETH: 10% -> **15%**
- DPI: 20% -> **35%**
- MAI (miMATIC): 10% -> **20%**

_Interest rate strategies_

For USDT, EURS, MAI and agEUR, the new parameters on their rate strategies are the following (all of them will share the same now):

- Optimal usage ratio: **80%**
- Variable rate slope 2: **75%**
- Stable rate slope 2: **75%**

For WETH, the new parameters on its rate strategy are the following:

- Optimal usage ratio: **80%**
- Base variable rate: **1%**
- Variable rate slope 1: **3.8%**
- Variable rate slope 2: **80%**
- Stable rate slope 1: **4%**
- Variable rate slope 2: **80%**
- Base stable rate offset: **3%**

**[Optimism](https://optimistic.etherscan.io/address/0x7902f3c60f05b5a6b7e4ce0cac11cb17bc8e607c#code#F21#L1)**

On Aave v3 Optimism, the proposal payload also includes 2 types of updates:

_Reserve Factors_

- WETH: 10% -> **15%**

_Interest rate strategies_

For USDT, the new parameters on its rate strategy are the following:

- Optimal usage ratio: **80%**
- Variable rate slope 2: **75%**
- Stable rate slope 2: **75%**

For WETH, the new parameters on its rate strategy are the following:

- Optimal usage ratio: **80%**
- Base variable rate: **1%**
- Variable rate slope 1: **3.8%**
- Variable rate slope 2: **80%**
- Stable rate slope 1: **4%**
- Variable rate slope 2: **80%**
- Base stable rate offset: **3%**

**[Arbitrum](https://arbiscan.io/address/0x7a9a9c14b35e58ffa1cc84ab421ace0fdcd289e3#code#F21#L1)**

Finally, on Aave v3 Arbitrum, the proposal payload also includes 2 types of updates:

_Reserve Factors_

- WETH: 10% -> **15%**

_Interest rate strategies_

For USDT and EURS the new parameters on their rate strategies (they share the same) are the following:

- Optimal usage ratio: **80%**
- Variable rate slope 2: **75%**
- Stable rate slope 2: **75%**

For WETH, the new parameters on its rate strategy are the following:

- Optimal usage ratio: **80%**
- Base variable rate: **1%**
- Variable rate slope 1: **3.8%**
- Variable rate slope 2: **80%**
- Stable rate slope 1: **4%**
- Variable rate slope 2: **80%**
- Base stable rate offset: **3%**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD wrote the payload.

:white_check_mark: With BGD writing the payload, at least another party reviewed it.
