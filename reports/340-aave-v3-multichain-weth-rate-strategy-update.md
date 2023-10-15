# Proposal 340. Aave v3 Arbitrum, Optimism - WETH interest rate update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=340](https://app.aave.com/governance/proposal/?proposalId=340)

<br>

### Governance forum discussion

[https://governance.aave.com/t/gauntlet-interest-rate-recommendations-for-weth-and-wmatic-on-v2-and-v3/14588/11](https://governance.aave.com/t/gauntlet-interest-rate-recommendations-for-weth-and-wmatic-on-v2-and-v3/14588/11)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the interest rate strategy of WETH on Aave v3 Arbitrum and Optimism.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x84c672e07feaf228035026fe8392699407b989800b8881aaef836ae9a2b934e0](https://etherscan.io/tx/0x84c672e07feaf228035026fe8392699407b989800b8881aaef836ae9a2b934e0)

```
- id: 340
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711,0xd1b3e25fd7c8ae7caddc6f71b461b79cd4ddcfa3]
- values: [0,0]
- signatures: [execute(address),execute(address)]
- calldatas: [0x000000000000000000000000c12ad8b3d242b1eddc1c8319d1d58608e67043ed,0x0000000000000000000000000568a3aeb8e78262deff75ee68fac20ae35ffa91]
- withDelegatecalls: [true,true]
- startBlock: 18333152
- endBlock: 18352352
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x72ff23d1f246eb05cb7fd1d111cec85e4139013465af2370701bfd29d7c544fe
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/340.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/340.md)

**Arbitrum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/340_Arbitrum_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/340_Arbitrum_pending_0.md)


**Optimism**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/340_Optimism_pending_1.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/340_Optimism_pending_1.md)

<br>

### Technical analysis

We have verified that, as presented in the specification, the following payloads properly update the base variable rate of WETH on Aave v3 Optimism and Arbitrum to **0%**.

[Arbitrum](https://arbiscan.io/address/0x0568a3aeb8e78262deff75ee68fac20ae35ffa91#code#F1#L19)

[Optimism](https://optimistic.etherscan.io/address/0xc12ad8b3d242b1eddc1c8319d1d58608e67043ed#code)


The proposal is consistent with the description on the governance forum.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

