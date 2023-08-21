# Proposal 302. Treasury Management - increase aUSDC position

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=302](https://app.aave.com/governance/proposal/?proposalId=302)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-deploy-ethereum-collector-contract/12205](https://governance.aave.com/t/arfc-deploy-ethereum-collector-contract/12205)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposal swaps different assets on the Aave Ethereum Collector to USDC and then deposits it into Aave v2 Ethereum, to get aUSDC v2.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x80f3563c80ef74444a863bf4aff6cca95b4f370a765c80bdf60345e9d1d0d2ef](https://etherscan.io/tx/0x80f3563c80ef74444a863bf4aff6cca95b4f370a765c80bdf60345e9d1d0d2ef)

```
- id: 302
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xea7c5a54453bb31bbd53c87ecd5dd7ff65839fc1]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17937985
- endBlock: 17957185
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xde9a6d8c0aeaa40afd8867b6b419757f2930551e0312ef47ad367676c1f96f3f
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/302.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/302.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xea7c5a54453bb31bbd53c87ecd5dd7ff65839fc1#code#F1#L18) does the following:


1. Deploys a COWSwapper contract, already used on previous treasury proposals to swap assets on the CowSwap/Milkman platforms. Its flow is generally similar as with proposal 267, explained in detail [HERE].
2. Withdraws a list of assets to swap to aUSDCv2 from the Aave Ethereum Collector, to the COWSwapper contract: sUSD, YFI, UNI, MKR, DAI, USDT, TUSD, GUSD, FRAX, LUSD, UST and TUSD.
3. Calls the `swap()` function in the COWSwapper contract for each asset, that will create the buy orders for USDC.
4. Transfer "pure" USDC (from RWA aUSDC) to COWSwapper, to join it with the resultant USDC of the swaps.

After the execution of the swap (already not part of the governance proposal), the COWSwapper contract will allow to deposit all the USDC contained there into Aave v2 Ethereum on behalf of the Aave v2 Ethereum Collector.

Same as with other treasury proposals, in order to protect the funds of the Aave DAO, our main focus regarding the CowTrader smart contract was on security of funds, lack of middle custody by off-chain parties and recoverability of assets in an emergency scenario. So we verified the following:
- Both the Aave Governance (via proposal) and the proposal submitter can cancel the trade, if the settlement would not happen. This is possible via the `cancelUsdt()` and `cancelDai()` functions included into CowTrader. Funds are then sent directly to the Aave Ethereum Collector, with no custody taken at any point by a third party in this cancellation scenario, including the proposer.
- As emergency mechanism, there is an extra function that allows to send any asset on the CowTrader to the Aave Ethereum Collector: `rescueTokens()`. Same as with the cancel functions, this is only callable by the proposal creator or the Aave Governance, with no middle custody step.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
