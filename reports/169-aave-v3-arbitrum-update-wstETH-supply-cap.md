# Proposal 169. Aave v3 Arbitrum - update wstETH supply cap

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=169](https://app.aave.com/governance/proposal/?proposalId=169)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-increase-supply-cap-for-wsteth-aave-arbitrum-v3/12163](https://governance.aave.com/t/arfc-increase-supply-cap-for-wsteth-aave-arbitrum-v3/12163)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal increases the supply cap of wstETH on Aave v3 Arbitrum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x517e9267cb2f09b954b2feafdbb1a5a6c7196e8d669be21faa86607f87b2294f](https://etherscan.io/tx/0x517e9267cb2f09b954b2feafdbb1a5a6c7196e8d669be21faa86607f87b2294f)

```
- id: 169
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x2e2b1f112c4d79a9d22464f0d345de9b792705f1]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000cdb9ea7f9443fa9e8ba6ebc9ef41c3ed75939663]
- withDelegatecalls: [true]
- startBlock: 16775470
- endBlock: 16794670
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x88483d979386f2743b5801e8875b6157d4ff776ca89e45173a5da22229b816a4
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/169.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/169.md)

**Arbitrum**

Aave Seatbelt doesn't support Arbitrum yet.

<br>

### Technical analysis

The [proposal payload](https://arbiscan.io/address/0xcdb9ea7f9443fa9e8ba6ebc9ef41c3ed75939663#code#F15#L1) simply interacts with the [PoolConfigurator](https://arbiscan.io/address/0x8145eddDf43f50276641b55bd3AD95944510021E) of Aave v3 Arbitrum to update the supply cap of wstETH from 1'200 wstETH to 2'400 wstETH by calling the `setSupplyCap()` function.

The proposal uses correctly the Aave cross-chain governance system to communicate with Arbitrum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
