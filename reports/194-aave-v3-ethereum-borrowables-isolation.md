# Proposal 194. Aave v3 Ethereum - enable assets to borrow in isolation

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=194](https://app.aave.com/governance/proposal/?proposalId=194)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-configure-isolation-mode-borrowable-assets-v3-ethereum/12420](https://governance.aave.com/t/arfc-configure-isolation-mode-borrowable-assets-v3-ethereum/12420)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal enables USDC, USDT, DAI and LUSD as borrowable against isolated collaterals on Aave v3 Ethereum.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x178a4dfd9d30e30c7282f399c062556571ed5330466f18a41bec18dd2ed9e9e5](https://etherscan.io/tx/0x178a4dfd9d30e30c7282f399c062556571ed5330466f18a41bec18dd2ed9e9e5)

```
- id: 194
- creator: 0xbc540e0729b732fb14afa240aa5a047ae9ba7df0
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xc2d768ef7dc088866b99b2b17af181f2debae9d4]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16962419
- endBlock: 16981619
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xc95042860f19868f3d7e57aea659418aaa4f8242ec3d47332ba5e49e1c9929f8
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/194.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/194.md)


<br>

### Technical analysis

The [proposal payload](https://etherscan.io/address/0xc2d768ef7dc088866b99b2b17af181f2debae9d4#code#F22#L1) correctly uses the new [BGD's Aave Config Engine of Aave v3 Ethereum](https://etherscan.io/address/0xE202F2fc4b6A37Ba53cfD15bE42a762A645FCA07#code#F18#L1), in this case, to enable USDT, USDC, DAI and LUSD as borrowable assets against isolated collaterals.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
