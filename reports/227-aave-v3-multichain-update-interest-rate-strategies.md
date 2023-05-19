# Proposal 227. Aave v3 Ethereum, Polygon, Optimism, Arbitrum - update rate strategies

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=227](https://app.aave.com/governance/proposal/?proposalId=227)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-aave-v3-interest-rate-curve-recommendations-from-gauntlet-2023-04-27/12921](https://governance.aave.com/t/arfc-aave-v3-interest-rate-curve-recommendations-from-gauntlet-2023-04-27/12921)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the interest rate strategies of multiple assets on Aave v3 Ethereum, Polygon, Optimism and Arbitrum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xefaaee516fda0fbbceb9fbb95ec230e57eea9c9676056d7cbe882228b1c378a7](https://etherscan.io/tx/0xefaaee516fda0fbbceb9fbb95ec230e57eea9c9676056d7cbe882228b1c378a7)

```
- id: 227
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xd1b3e25fd7c8ae7caddc6f71b461b79cd4ddcfa3,0xfc7b55cc7c5bd3ae89ac679c7250ab30754c5cc5,0x158a6bc04f0828318821bae797f50b0a1299d45b,0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711]
- values: [0,0,0,0]
- signatures: [execute(address),execute(),execute(address),execute(address)]
- calldatas: [0x000000000000000000000000f4d1352b3e9e99fca6aa20f62fe95192a26c9527,0x,0x0000000000000000000000001cdb984008dcee9d06c28654ed31cf82680eea62,0x000000000000000000000000ac63290bc16fbc33353b14f139cef1c660ba56f0]
- withDelegatecalls: [true,true,true,true]
- startBlock: 17276670
- endBlock: 17295870
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x16eb4b2816ebae6591136eb3c36e58bd1c92a2d1603c04ecce25a7ac07732573
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/227.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/227.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/227_fx_39_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/227_fx_39_0.md)

**Optimism**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/227_optimism_17_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/227_optimism_17_0.md)

**Arbitrum**

Aave Seatbelt doesn't support Arbitrum yet.

<br>

### Technical analysis

We have verified that on the non-Ethereum payloads, the proposal uses correctly the Aave cross-chain governance system to communicate with Polygon, Optimism and Arbitrum.

Regarding the independent payloads, they do the following:

**[Ethereum payload](https://etherscan.io/address/0xfc7b55cc7c5bd3ae89ac679c7250ab30754c5cc5#code#F1#L85)**

- CRV
  - Reserve Factor: 20% -> **35%**

- USDC
  - Interest rate strategy:
    - Variable slope 1: 4% -> **3.5%**

- USDT
  - Interest rate strategy:
    - Optimal usage: 90% -> **80%**
    - Variable slope 2: 72% -> **75%**

- WBTC
  - Interest rate strategy:
    - Variable slope 1: 7% -> **4%**


**[Polygon](https://polygonscan.com/address/0x1cdb984008dcee9d06c28654ed31cf82680eea62#code#F1#L159)**

- CRV
  - Reserve Factor: 20% -> **35%**

- DPI
  - Interest rate strategy:
    - Variable slope 1: 7% -> **10%**

- EURS
  - Interest rate strategy:
    - Variable slope 1: 4% -> **6%**

- USDC
  - Interest rate strategy:
    - Variable slope 1: 4% -> **3.5%**

- WBTC
  - Interest rate strategy:
    - Variable slope 1: 7% -> **4%**

**[Optimism](https://optimistic.etherscan.io/address/0xac63290bc16fbc33353b14f139cef1c660ba56f0#code#F1#L250)**

- USDC
  - Interest rate strategy:
    - Variable slope 1: 4% -> **3.5%**

- WBTC
  - Interest rate strategy:
    - Variable slope 1: 7% -> **4%**

**[Arbitrum](https://arbiscan.io/address/0xf4d1352b3e9e99fca6aa20f62fe95192a26c9527#code#F1#L37)**

- EURS
  - Interest rate strategy:
    - Variable slope 1: 4% -> **6%**

- USDC
  - Interest rate strategy:
    - Variable slope 1: 4% -> **3.5%**

- WBTC
  - Interest rate strategy:
    - Variable slope 1: 7% -> **4%**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Multiple payloads used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
