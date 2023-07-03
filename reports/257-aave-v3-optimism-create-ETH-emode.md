# Proposal 257. Aave v3 Optimism - create ETH-correlated e-mode category

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=257](https://app.aave.com/governance/proposal/?proposalId=257)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-optimism-create-eth-e-mode/13144](https://governance.aave.com/t/arfc-optimism-create-eth-e-mode/13144)

<br>

## BGD analysis

<br>

### Proposal types

:zap: emode

<br>

### Context

This proposal creates the ETH-correlated e-mode category on Aave v3 Optimism, and adds WETH and wstETH to it.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xa682f386d1b9e24ad353091b328f9c73be55e176ac2d0cdb8a172f0c8dabaccf](https://etherscan.io/tx/0xa682f386d1b9e24ad353091b328f9c73be55e176ac2d0cdb8a172f0c8dabaccf)

```
- id: 257
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x00000000000000000000000080cb7e9e015c5331bf34e06de62443d070fd6654]
- withDelegatecalls: [true]
- startBlock: 17593463
- endBlock: 17612663
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xd5edeaa37f402f3fca8190927699519ef5a8b81285aca97a276f871d8d2ae201
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/257.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/257.md)

**Optimism**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/257_Optimism_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/257_Optimism_pending_0.md)

<br>

### Technical analysis

We have verified the proposal interacts correctly with the Aave cross-chain governance system, in its connection with Optimism.

Regarding the [proposal payload](https://optimistic.etherscan.io/address/0x80cb7e9e015c5331bf34e06de62443d070fd6654#code#F1#L15), we have verified it does the following:

First, it creates a new ETH-correlated e-mode with the following specifications:
- LTV: 90%
- Liquidation Threshold: 93%
- Liquidation Bonus: 1%
- Id: 2

This is done by calling the `setEModeCategory()` function on the [Aave v3 Optimism Pool Configurator contract](https://optimistic.etherscan.io/address/0x8145eddDf43f50276641b55bd3AD95944510021E).

After that, it adds to this new e-mode the eligible assets on Aave v3 Optimism: WETH and wstETH. 
This is done by calling the `setAssetEModeCategory()` function on the Aave v3 Optimism Pool Configurator too.

<br>

There is an inconsistency between the proposal payload and the description on AIP & forum: the Id suggested for the new e-mode category is `1`, but it should be `2`, as `1` already belongs to the stablecoins category.
**We can confirm the proposal payload correctly updates it to `2`, not creating any clash of ids**


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
