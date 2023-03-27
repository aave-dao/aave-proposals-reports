# Proposal 186. Aave v3 Polygon, Arbitrum - update of supply/borrow caps

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=186](https://app.aave.com/governance/proposal/?proposalId=186)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-supply-and-borrow-caps-update-wsteth-v3-arbitrum/12309](https://governance.aave.com/t/arfc-supply-and-borrow-caps-update-wsteth-v3-arbitrum/12309)

[https://governance.aave.com/t/arfc-chaos-labs-supply-and-borrow-cap-updates-aave-v3-polygon-2023-03-16/12310](https://governance.aave.com/t/arfc-chaos-labs-supply-and-borrow-cap-updates-aave-v3-polygon-2023-03-16/12310)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates multiple supply and borrow caps on Aave v3 Polygon and Arbitrum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x3b49bed5329cccb61331c553171b678d87f512265d59ae1307a0745a1798f257](https://etherscan.io/tx/0x3b49bed5329cccb61331c553171b678d87f512265d59ae1307a0745a1798f257)

```
- id: 186
- creator: 0xbc540e0729b732fb14afa240aa5a047ae9ba7df0
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x2e2b1f112c4d79a9d22464f0d345de9b792705f1,0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0,0]
- signatures: [execute(address),execute(address)]
- calldatas: [0x000000000000000000000000656482165fdf78f3fdd31d4ad4b518350766f3d5,0x000000000000000000000000656482165fdf78f3fdd31d4ad4b518350766f3d5]
- withDelegatecalls: [true,true]
- startBlock: 16876996
- endBlock: 16896196
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xb2323bc2ec23771a8e717c51e02debd7b72ec25f97cbbc5f66a8dbc979acff3f
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/186.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/186.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/186_fx_22_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/186_fx_22_0.md)


**Arbitrum**

Aave Seatbelt doesn't support Arbitrum yet.

<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Polygon and Arbitrum.
The proposals payloads do the following:

**[Polygon](https://polygonscan.com/address/0x656482165fdf78f3fdd31d4ad4b518350766f3d5#code#F15#L1)**

By calling the [PoolConfigurator of Aave v3 Polygon](https://polygonscan.com/address/0x8145eddDf43f50276641b55bd3AD95944510021E) it changes the following caps:

- MAI (miMATIC) supply cap: 1'100'000 MAI -> **2'200'000 MAI**
- MAI (miMATIC) borrow cap: 600'000 MAI -> **1'200'000 MAI**
- stMATIC supply cap: 15'000'000 stMATIC -> **21'000'000 stMATIC** 

<br>

**[Arbitrum](https://arbiscan.io/address/0x656482165fdf78f3fdd31d4ad4b518350766f3d5#code#F15#L1)**

By calling the [PoolConfigurator of Aave v3 Arbitrum](https://arbiscan.io/address/0x8145eddDf43f50276641b55bd3AD95944510021E) it changes the following caps:

- wstETH supply cap: 2'400 wstETH -> **4'650 wstETH**
- wstETH borrow cap: 190 wstETH -> **400 wstETH**


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
