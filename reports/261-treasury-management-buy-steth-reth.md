# Proposal 261. Treasury Management - swap ETH Collector holdings to stETH and rETH

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=261](https://app.aave.com/governance/proposal/?proposalId=261)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-deploy-ethereum-collector-contract/12205/5](https://governance.aave.com/t/arfc-deploy-ethereum-collector-contract/12205/5)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposal swaps ETH/WETH and different flavors of ETH aTokens held by the Aave Collector into ETH LSTs: stETH and rETH.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x4a7e0a065ae7f64e1a56615332afac8524d9fe55fa23b0dba963fbb21a1b7d86](https://etherscan.io/tx/0x4a7e0a065ae7f64e1a56615332afac8524d9fe55fa23b0dba963fbb21a1b7d86)

```
- id: 261
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xe5b5b70f9a5ccc2841f9facbb0c5c6030e68f341]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17621656
- endBlock: 17640856
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xaad64e6d09cc64d0f350138f8b0bdd707b659fc6eee1ff6a9ceacc29bc9fa099
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/261.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/261.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xe5b5b70f9a5ccc2841f9facbb0c5c6030e68f341#code) does the following:

- First, it defines a target of 1'600 value of ETH to swap: 800 will be deposited into wstETH, 800 on rETH.
- Second, it sources from the Collector to the Executor contract (who will be doing the deposit into wstETH and rETH) the required ETH the following way:
  - 1'400 ETH will be sourced from aWETH Aave v2.
  - ~104.5 ETH will be sourced from ETH contained in the Aave Collector.
  - The rest up to 1'600 will be sourced from aWETH Aave v3.
  We have verified all balances should be enough to cover the sourcing of funds.
- Afterwards, 800 ETH are deposited into rETH and another 800 first on stETH and then wrapped into wstETH.
- Finally, the rETH and wstETH is transferred to the Aave Collector.

Given that when doing transfers of aTokens small imprecisions on the wei order of magnitude could be expected, we have also checked that the small amount of ETH present on the Level 1 Executor is enough to cover them.

The proposal payload is consistent with [Snapshot](https://snapshot.org/#/aave.eth/proposal/0x5bcb6dddf3e65597db2f0e8300edca5737788fcf6c63ca90024a8b4e685b40fe) and the forum description.



<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
