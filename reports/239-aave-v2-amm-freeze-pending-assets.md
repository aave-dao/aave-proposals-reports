# Proposal 239. Aave v2 Ethereum AMM - Freezing of all non-frozen assets

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=239](https://app.aave.com/governance/proposal/?proposalId=239)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-deprecate-aave-v2-amm-market/12830](https://governance.aave.com/t/arfc-deprecate-aave-v2-amm-market/12830)

<br>

## BGD analysis

<br>

### Proposal types

:ice_cube: freeze-asset

<br>

### Context

Following the freezing of all LP assets on Aave v2 Ethereum AMM, this proposal progresses with the deprecation of the pool by freezing the rest: DAI, USDC, USDT, WBTC and ETH.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xeaa34da7a004c4db88213a510a11edc81adf7c840ddaa896a7773416964d78bb](https://etherscan.io/tx/0xeaa34da7a004c4db88213a510a11edc81adf7c840ddaa896a7773416964d78bb)

```
- id: 239
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x23a875ede3f1030138701683e42e9b16a7f87768,0x23a875ede3f1030138701683e42e9b16a7f87768,0x23a875ede3f1030138701683e42e9b16a7f87768,0x23a875ede3f1030138701683e42e9b16a7f87768,0x23a875ede3f1030138701683e42e9b16a7f87768]
- values: [0,0,0,0,0]
- signatures: [freezeReserve(address),freezeReserve(address),freezeReserve(address),freezeReserve(address),freezeReserve(address)]
- calldatas: [0x000000000000000000000000c02aaa39b223fe8d0a0e5c4f27ead9083c756cc2,0x0000000000000000000000006b175474e89094c44da98b954eedeac495271d0f,0x000000000000000000000000a0b86991c6218b36c1d19d4a2e9eb0ce3606eb48,0x000000000000000000000000dac17f958d2ee523a2206206994597c13d831ec7,0x0000000000000000000000002260fac5e5542a773aa44fbcfedf7c193bc2c599]
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/239.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/239.md)


<br>

### Technical analysis

The proposal payload (submitted via calldata) interacts with the [Aave v2 Ethereum AMM Pool Configurator](https://etherscan.io/address/0x23a875ede3f1030138701683e42e9b16a7f87768) to call the `freezeReserve()` on WBTC, DAI, USDC, WETH and USDT, effectively freezing those assets: not allowing more supplying and borrowing.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: Payload encoded via multiple targets and calldatas, no delegatecall

:x: BGD reviewed the payload before the proposal was submitted.

:x: BGD reviewed the procedure followed to submit the proposal.
