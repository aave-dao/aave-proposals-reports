# Proposal 76. Consolidate Reserve Factors and Enable Borrowing DPI

<br>

### Voting link
[https://app.aave.com/governance/proposal/?proposalId=76](https://app.aave.com/governance/proposal/?proposalId=76)

### Governance forum discussion
[https://governance.aave.com/t/arc-consolidate-aave-v1-v2-amm-reserve-factors-purchase-cvx-and-deploy-to-earn-yield/6797](https://governance.aave.com/t/arc-consolidate-aave-v1-v2-amm-reserve-factors-purchase-cvx-and-deploy-to-earn-yield/6797)

<br>

## BGD analysis

### Proposal types

:wrench: :arrow_up: contract-implementation-upgrade

:wrench: :bar_chart: params-update

### Context
This proposal "redirects" the flow of funds from the Aave v1 ecosystem's reserve to the Aave v2 Ethereum ecosystem's reserve.

It also re-enables borrowing of DPI on Aave v2 Ethereum.

### Proposal creation
Transaction: [https://etherscan.io/tx/0x88e51deddbb3527027f104e0c5d15d335c42981a6b8d90cf18191c8e2fa7fb2a](https://etherscan.io/tx/0x88e51deddbb3527027f104e0c5d15d335c42981a6b8d90cf18191c8e2fa7fb2a)
```
- id: 76
- creator: 0x5b3bffc0bcf8d4caec873fdcf719f60725767c98
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x43d2a74c55ee4db917251ec934b2fd03e3069bd6,0x43d2a74c55ee4db917251ec934b2fd03e3069bd6]
- values: [0,0]
- signatures: [execute(),distributeTokens()]
- calldatas: [0x,0x]
- withDelegatecalls: [true,false]
- startBlock: 14793371
- endBlock: 14812571
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xb9c608ca7bc75d445c771464870514b2a829823713e5efc7e7ca713054f8ead6
```

### Technical analysis
From a technical perspective, this proposal has 4 parts:

<br>

**(1) Aave Ecosystem's Reserve v1 upgrade**

The ecosystem reserve of Aave v1 is a smart contract named [TokenDistributor](https://etherscan.io/address/0xe3d9988f676457123c5fd01297605efdd0cba1ae#code), which for legacy reason, requires an upgrade of its implementation to update the address to which the funds stored there can be distributed. The payload of this proposal upgrades the proxy of the ecosystem reserve with a new implementation of [TokenDistributor](https://etherscan.io/address/0x55c559730cbCA5deB0bf9B85961957FfDf502603#code), whose only change is the increase of its REVISION from 5 to 6.

When upgrading the implementation, a new distribution is defined, to set as recipient of all the funds the [ecosystem reserve of Aave v2 Ethereum](https://etherscan.io/address/0x464C71f6c2F760DdA6093dCB91C24c39e5d6e18c).

After the step that we will present on 2), this contract will not receive more funds (as the fees from v1 will go directly to v2's ecosystem reserve), but this change of distribution is done for then to release ~$650'000 accumulated there.

<br>

**(2) Redirection of v1 fees to Aave ecosystem's reserve of v2**

As the goal is to not accrue anymore fees of v1 on the v1 ecosystem reserve, but on v2's, the payload sets as recipient of the v1 fees, the v2 ecosystem's reserve, by calling `setTokenDistributor()` on the pool addresses provider of v1.

<br>

**(3) Re-enabling DPI borrowing on Aave v2 Ethereum**

Not related with the previous, but finally the payload also enables borrowing for DPI on Aave v2 Ethereum, by properly calling `enableBorrowingOnReserve()` on the pool configurator of Aave v2 Ethereum. Stable rate, as before, is not enabled.

<br>

**(4) Distribute of v1 leftovers to v2's ecosystem's reserve**

Finally, after the distribution for v1's reserve's ecosystem was changed to point to v2's, the proposal does a call to `distribute()` on the TokenDistributor, that will send all the funds accrued there to v2.

<br>

----

<br>

It is important to highlight that these funds will not be in the form of aTokens (so not growing), but the proposer has confirmed to BGD that it's on scope of the next phase of this project to optimize that.

Another interesting aspect of this proposal is the usage of a delegatecall + call pattern, in order to include the whole logic in the same contract. This is correct, but generally we don't recommend to combine heavily delegatecall + call, as it is more prone to mistakes.

<br>
<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed that the contract update doesn't affect proxy's storage layout.

:white_check_mark: BGD reviewed that there is no attack involving a non-initialized proxy's implementation.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

:white_check_mark: Only one payload used via delegatecall + call
