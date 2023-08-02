# Proposal 282. Treasury Management - increase aUSDC position

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=282](https://app.aave.com/governance/proposal/?proposalId=282)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-deploy-ethereum-collector-contract/12205](https://governance.aave.com/t/arfc-deploy-ethereum-collector-contract/12205)

*This discussion is slightly outdated, and not reflecting in detail the proposal payload itself, even if aligned*

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposal "rebalances" stablecoin held by the Aave Collector, from USDC, aUSDT v2 and aDAI v2, to aUSDC v2.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x512f55f9ab84afbe9c40b57e1c76d1ecd49aec3d403b533ea8e7d0d39cea67b9](https://etherscan.io/tx/0x512f55f9ab84afbe9c40b57e1c76d1ecd49aec3d403b533ea8e7d0d39cea67b9)

```
- id: 282
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x7a2fa9c7beb9f8518373f0f63e3cc75b5b4dd3c7]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17800452
- endBlock: 17819652
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x1299fb210c9383714d62dc5662d32ecd457751b541738743c38af2df1e4c10e5
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/282.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/282.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x7a2fa9c7beb9f8518373f0f63e3cc75b5b4dd3c7#code#F1#L18) does the following:

Regarding the operations not requiring interaction with 3rd party asset swap platform, the proposal deposits the USDC holdings of the Aave Ethereum Collector (~297'000 USDC at the moment) into Aave v2 Ethereum on behalf of the Collector, for it to receive aUSDC v2.

The second component of the payload is initiating a swap of aUSDT v2 (974'000 USDT) and aDAI v2 (974'000) to (after some middle step) aUSDC v2.

This swap is executed via a COWSwapper smart contract, integrated with the CowSwap platform. Its flow is generally similar as with proposal 267, explained in detail [HERE](./267-treasury-management-bal-weth.md), but in summary:
1. The proposal payload sends DAI and USDT to the COWSwap contract.
2. The proposal payload calls the `swap()`function on COWSwapper.
3. `swap()` interacts with Milkman (a system on top of CowSwap to do validations at settlement time) to create 2 orders: one to swap USDT to USDC, another to swap DAI to USDC.

The validation of internal workings of Milkman and CowSwap are out of our review scope, but the usage of `ChainlinkExpectedOutCalculator` as price checker for Milkman, and the USDT, DAI and USDC Chainlink oracles as reference, looks legitimate.
Integration details with CowSwap are also out of out scope.

Once the trade orders are created on Milkman, the execution stage of the governance proposal ends, and the flow passes off-chain to CoWSwap.

The flow on settlement stage is the following:
1. Once the off-chain orders are filled, the CowSwapper contract should receive the USDC.
2. Then, a permissionless `depositIntoAaveV2()` function can be called by any address, that will deposit the held USDC into Aave v2 Ethereum on behalf of the Collector.

Same as with proposal 267, in order to protect the funds of the Aave DAO, our main focus regarding the CowTrader smart contract was on security of funds, lack of middle custody by off-chain parties and recoverability of assets in an emergency scenario. So we verified the following:
- Both the Aave Governance (via proposal) and the proposal submitter can cancel the trade, if the settlement would not happen. This is possible via the `cancelUsdt()` and `cancelDai()` functions included into CowTrader. Funds are then sent directly to the Aave Ethereum Collector, with no custody taken at any point by a third party in this cancellation scenario, including the proposer.
- As emergency mechanism, there is an extra function that allows to send any asset on the CowTrader to the Aave Ethereum Collector: `rescueTokens()`. Same as with the cancel functions, this is only callable by the proposal creator or the Aave Governance, with no middle custody step.

Same as with the forum thread, the [Snapshot referenced on the payload](https://snapshot.org/#/aave.eth/proposal/0xb4141f12f7ec8e037e6320912b5673fcc5909457d9f6201c018d5c15e5aa5083) is outdated and pointing to more general (and not precise content), even if aligned.
Given this proposal comes from an engaged service provider into treasury management, we think it is still legitimate.



<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:-: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
