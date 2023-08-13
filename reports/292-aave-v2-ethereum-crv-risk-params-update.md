# Proposal 292. Aave v2 Ethereum - CRV risk parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=292](https://app.aave.com/governance/proposal/?proposalId=292)

<br>

### Governance forum discussion

[https://governance.aave.com/t/post-vyper-exploit-crv-market-update-and-recommendations/14214/43](https://governance.aave.com/t/post-vyper-exploit-crv-market-update-and-recommendations/14214/43)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal reduces the Liquidation Threshold (LT) of CRV by 6% on Aave v2 Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x57cb507317fdae61c9ca98b457dfe8b338336b36d7ac17a124f1fb51d0547261](https://etherscan.io/tx/0x57cb507317fdae61c9ca98b457dfe8b338336b36d7ac17a124f1fb51d0547261)

```
- id: 292
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xaf07c70420f6471329b5a32f0fa77776fba7147c]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17883658
- endBlock: 17902858
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xf3f1a5c3cdd7988a70e0add08acbdd5fe2494c31654bda232552d04634793da6
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/292.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/292.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xaf07c70420f6471329b5a32f0fa77776fba7147c#code#F1#L14) properly reduces the LT of CRV to **49%** (from 55%) on Aave v2 Ethereum, by interacting with the Pool Configurator contract.

The proposal is consistent with the discussions on the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
