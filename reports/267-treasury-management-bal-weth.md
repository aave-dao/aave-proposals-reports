# Proposal 267. Treasury Management - acquire B-80BAL-20WETH

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=267](https://app.aave.com/governance/proposal/?proposalId=267)

<br>

### Governance forum discussion

[https://governance.aave.com/t/deploy-bal-abal-from-the-collector-contract/9747](https://governance.aave.com/t/deploy-bal-abal-from-the-collector-contract/9747)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposal uses WETH and aBAL held by the Aave Ethereum Collector to acquire Balance B-80BAL-20WETH for the Aave DAO, to be used for voting on Balancer in the future.

This is a 2-steps proposal, with the second step happening after the proposal execution, partially off-chain on the CowSwap platform.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xe6a1296c324bc275819005271b5c639898764c156b32f67163e9c9d1fd4617a6](https://etherscan.io/tx/0xe6a1296c324bc275819005271b5c639898764c156b32f67163e9c9d1fd4617a6)

```
- id: 267
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x11cdf91b0357d236f39d319091b21fbaed88b037]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17637660
- endBlock: 17656860
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xd1ad8ad41f5f2483c2f18e3c16a85bd87c9aa82f92ff584d27027dd6dec656b0
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/267.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/267.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x11cdf91b0357d236f39d319091b21fbaed88b037#code#F1#L20) does the following:

- In terms of outflow of assets, the WETH amount is fixed to 326.88 WETH, while the amount of BAL is taken dynamically from the balance of the Aave Ethereum Collector of aBAL (v2 and v3). Given that this is a follow-up step of a previous BAL acquisition, and that the balance of BAL deposited on Aave doesn't increase meaningfully, this is an acceptable assumption.
The amount of BAL is in the order of ~310'000 BAL.
- The payload deploys a CowTrader smart contract, the core of the proposal. More on this later.
- As next step, the WETH and the aBAL (v2/v3) are withdrawn from their respective Aave versions, and transferred to the just deployed CowTrader smart contract.
- Finally, the `trade()` function is called on the CowTrader contract.

**`trade()` on CowTrader**

In order to acquire b-80BAL-20WETH and be protected price-wise (MEV), the swap is done via the CowSwap platform, which implements an auction system based on off-chain matching.
Additionally, the Milkman system built on top of CowSwap is used, which allows to introduce extra on-chain validations (in this case, based on a on-chain oracle) at the settlement moment. This is useful in order to remove trust from any off-chain component of CowSwap.

Given that the scope of an Aave proposal review can't take into account all the internal workings of an external platform, the following assumptions are done:
- The price checker required by Milkman is correct, and the team submitting the proposal (Llama) properly evaluated it.
- Apart from simulation testing (that BGD is able to review), the team submitting the proposal (Llama) properly tested similar scenarios. This is important due to the off-chain components involved in the swap, not possible otherwise.
- The integration with CowSwap and Milkman is correct, and their teams reviewed it at request of the team submitting the proposal (Llama).

Regarding the flow on the CowTrader smart contract, the following happens:
1. Once funds are received from the payload execution, the Aave Level 1 Executor (Short Executor), calls `trade()`. Internally, the function approves the [Milkman smart contract](https://etherscan.io/address/0x11C76AD590ABDFFCD980afEC9ad951B160F02797) for BAL and WETH, and request two trades via the `requestSwapExactTokensForTokens()`: WETH -> B-80BAL-20WETH and BAL -> B-80BAL-20WETH. The rationale of executing via two separate trades (for what the proposal creator (Llama) explained us) is a matter of efficiency due to CowSwap's auction system works. We assume proper due diligence on the fact was done.
2. Within the context of `requestSwapExactTokensForTokens()`, the Milkman contract will pull the WETH and BAL funds, and lock them, in order to enforce the validations defined in the so-called [PriceChecker smart contract](https://etherscan.io/address/0xBeA6AAC5bDCe0206A9f909d80a467C93A7D6Da7c#code).

In order to protect the funds of the Aave DAO, our main focus regarding the CowTrader smart contract was on security of funds of the DAO, lack of middle custody by off-chain parties and recoverability of assets in an emergency scenario. So we verified the following:
- Both the Aave Governance (via proposal) and the proposal submitter can cancel the trade, if the settlement would not happen. This is possible via the `cancelTrades()` function included into CowTrader. Funds are then sent directly to the Aave Ethereum Collector, with no custody taken at any point by a third party in this cancellation scenario, including the proposer.
- As emergency mechanism, there is an extra function that allows to send any asset on the CowTrader to the Aave Ethereum Collector: `rescueTokens()`. Same as with `cancelTrades()`, this is only callable by the proposal creator or the Aave Governance, with no middle custody step.


The proposal payload is consistent with [Snapshot](https://snapshot.org/#/aave.eth/proposal/0x05182d6092e7a075b94ab937a6cd57968f36c6ac225196561a58b437e591065f) and the forum description, with small divergences in amounts, which seem acceptable.



<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
