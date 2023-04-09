# Proposal 198. Aave v3 Polygon, Arbitrum - update of debt ceilings

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=198](https://app.aave.com/governance/proposal/?proposalId=198)

<br>

### Governance forum discussion

[https://governance.aave.com/t/gauntlet-aave-v3-isolation-mode-methodology/12290](https://governance.aave.com/t/gauntlet-aave-v3-isolation-mode-methodology/12290)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates debt ceilings on Aave v3 Polygon and Arbitrum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x14968841da033215afb979a08a8ca55b25473e6cb162981e1dc6958b0e3d4bb1](https://etherscan.io/tx/0x14968841da033215afb979a08a8ca55b25473e6cb162981e1dc6958b0e3d4bb1)

```
- id: 198
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b,0xd1b3e25fd7c8ae7caddc6f71b461b79cd4ddcfa3]
- values: [0,0]
- signatures: [execute(address),execute(address)]
- calldatas: [0x0000000000000000000000006bce15b789e537f3aba3c60cb183f0e8737f05ec,0x0000000000000000000000004393277b02ef3ca293990a772b7160a8c76f2443]
- withDelegatecalls: [true,true]
- startBlock: 16985017
- endBlock: 17004217
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xc3d2121ca8e90ce2bc2e715bec74f92cb2241e1b88a338a855661865402e2ea7
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/198.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/198.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/198_fx_25_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/198_fx_25_0.md)

**Arbitrum**

Aave Seatbelt doesn't support Arbitrum yet.

<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Polygon and Arbitrum.
The proposals payloads do the following:

**[Polygon](https://polygonscan.com/address/0x6bce15b789e537f3aba3c60cb183f0e8737f05ec#code#F23#L1)**

This payload is correctly created with the new [BGD's Aave Config Engine of Aave v3 Polygon](https://polygonscan.com/address/0xe202f2fc4b6a37ba53cfd15be42a762a645fca07#code#F18#L1) as target, doing the following changes:

- EURS debt ceiling: 5'000'000 USD -> **675'000 USD**

<br>

**[Arbitrum](https://arbiscan.io/address/0x4393277b02ef3ca293990a772b7160a8c76f2443#code#F23#L16)**

This payload is also correctly created with the new [BGD's Aave Config Engine of Aave v3 Arbitrum](https://arbiscan.io/address/0x0efdfc1a940de4e7e6acc9bb801481f81b17fd20#code#F18#L1) as target, doing the following changes:

- USDT debt ceiling: 5'000'000 USD -> **2'500'000 USD**
- EURS debt ceiling: 5'000'000 USD -> **25'000 USD**


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
