# Proposal 200. Aave v3 Arbitrum - wstETH caps update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=200](https://app.aave.com/governance/proposal/?proposalId=200)

<br>

### Governance forum discussions

[https://governance.aave.com/t/arc-gauntlet-recommendations-for-wsteth-on-aave-v3-arbitrum/12675](https://governance.aave.com/t/arc-gauntlet-recommendations-for-wsteth-on-aave-v3-arbitrum/12675)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the borrow of wstETH on Aave v3 Arbitrum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xa78debdb926b33272734e6c30c4279a3d75c0fac217a4b6511479f7f33fd26dc](https://etherscan.io/tx/0xa78debdb926b33272734e6c30c4279a3d75c0fac217a4b6511479f7f33fd26dc)

```
- id: 200
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xd1b3e25fd7c8ae7caddc6f71b461b79cd4ddcfa3]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x00000000000000000000000031976dc2ea27e75cc5a3687ed594d17127f9b72e]
- withDelegatecalls: [true]
- startBlock: 17028565
- endBlock: 17047765
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x464496497d766fa1724c5fb3e6f501d7c89ed662109536184efdf6d925789186
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/200.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/200.md)

**Arbitrum**

Aave Seatbelt doesn't support Arbitrum yet.

<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Arbitrum.

Regarding the Arbitrum side, we have verified the [proposal payload](https://arbiscan.io/address/0x31976DC2Ea27E75cC5a3687ED594D17127f9b72E#code#F21#L1) correctly updates the borrow cap of wstETH from 400 wstETH to 800 wstETH.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
