# Proposal 295. Aave v3 Polygon, Arbitrum, Optimism - wstETH caps update

<br>


### Voting link

[https://app.aave.com/governance/proposal/?proposalId=295](https://app.aave.com/governance/proposal/?proposalId=295)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-supply-cap-increase-wsteth/14376](https://governance.aave.com/t/arfc-supply-cap-increase-wsteth/14376)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the supply caps of wstETH across Aave v3 Polygon, Arbitrum and Optimism.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x0b1599bc3802eb8fab73a8dde7a0649c3686854a4191dd5a285ed5e7d5b1bb78](https://etherscan.io/tx/0x0b1599bc3802eb8fab73a8dde7a0649c3686854a4191dd5a285ed5e7d5b1bb78)

```
- id: 295
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711,0xd1b3e25fd7c8ae7caddc6f71b461b79cd4ddcfa3,0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0,0,0]
- signatures: [execute(address),execute(address),execute(address)]
- calldatas: [0x000000000000000000000000f285e2d9c5cdaab11c167ffa70fa4055fbeaed96,0x00000000000000000000000083a67159a0ad5612178bed9deb43c0f58e941932,0x000000000000000000000000af6568bd3923e2ad05a0d6e4206f601d08e0cde2]
- withDelegatecalls: [true,true,true]
- startBlock: 17894289
- endBlock: 17913489
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x71762c3ee22bbd69aa2da5717e88508076bd0b7e6467feb8d1e8907f565ccdae
```

<br>

### Aave Seatbelt reports

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/295.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/295.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/295_Polygon_pending_1.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/295_Polygon_pending_1.md)


**Arbitrum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/295_Arbitrum_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/295_Arbitrum_pending_0.md)

**Optimism**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/295_Optimism_pending_2.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/295_Optimism_pending_2.md)

<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Polygon, Arbitrum and Optimism.

From a technical perspective, we have verified the proposal payloads do the following updates:

[Polygon](https://polygonscan.com/address/0xaf6568bd3923e2ad05a0d6e4206f601d08e0cde2#code#F1#L13)

**wstETH**

- Supply cap: 2'700 wstETH -> **3'450 wstETH**


[Arbitrum](https://arbiscan.io/address/0x83a67159a0ad5612178bed9deb43c0f58e941932#code#F1#L13)

**wstETH**

- Supply cap: 30'000 wstETH -> **45'000 wstETH**


[Optimism](https://optimistic.etherscan.io/address/0xf285e2d9c5cdaab11c167ffa70fa4055fbeaed96#code#F1#L13)

**wstETH**

- Supply cap: 23'000 wstETH -> **34'500 wstETH**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
