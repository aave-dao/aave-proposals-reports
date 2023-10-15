# Proposal 343. Treasury Management - Fund GLC (GHO Liquidity Committee) with GHO budget

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=343](https://app.aave.com/governance/proposal/?proposalId=343)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-treasury-manage-gho-liquidity-committee/14914](https://governance.aave.com/t/arfc-treasury-manage-gho-liquidity-committee/14914)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposals swaps 406'000 aDAI to GHO via the AaveSwapper contract, in order to funds operations of the GLC (GHO Liquidity Committee) during 3 months.

Additionally, it transfer 5 ETH to the GLC.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x7bda484db86c76b0b6c187ecf6819d0d781d3e31f6ed97ff3575bd2080bbb8e8](https://etherscan.io/tx/0x7bda484db86c76b0b6c187ecf6819d0d781d3e31f6ed97ff3575bd2080bbb8e8)

```
- id: 343
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x5f8cb9a8e12377aae2f534813c51eec7e36d2772]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 18335161
- endBlock: 18354361
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x7d076567e9e53a9bd05d90d7a42fd2d9ed17bccf58caf9da25eafe3acb3177e8
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/343.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/343.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x5f8cb9a8e12377aae2f534813c51eec7e36d2772#code#F1#L37) does the following:


1. The payload redeems 406'000 DAI and 5 WETH from the Aave Ethereum Collector (held in aDAI and aWETH).
2. By interacting with the AaveSwapper smart contract, the payload creates 1 order to swap DAI to GHO, that will be received by the Aave Ethereum Collector.
3. Redeems the 5 ETH from WETH, and sends it to the GLC address.
4. Approves the GLC address to pull 406'000 GHO from the Aave Ethereum Collector.

After the payload is executed, off-chain the AaveSwapper will execute the swap to GHO via CowSwap/Milkman, and transfer the funds to the Aave Ethereum Collector. At that point, the GLC will be able to claim funds, if there are no available GHO funds before.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
