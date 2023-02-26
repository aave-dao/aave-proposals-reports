# Proposal 164. Aave v3 Optimism - Risk Parameter Updates 

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=164](https://app.aave.com/governance/proposal/?proposalId=164)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-gauntlet-risk-parameter-updates-for-avax-v3-and-op-v3-2023-02-16/11940](https://governance.aave.com/t/arc-gauntlet-risk-parameter-updates-for-avax-v3-and-op-v3-2023-02-16/11940)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal is an update of risk parameters on Aave v3 Optimism, affecting WBTC and sUSD.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xf46f57f5ff00711b4bfd0825e662e8cbb4c7d1d927139be87d7474ac4e9d1cd2](https://etherscan.io/tx/0xf46f57f5ff00711b4bfd0825e662e8cbb4c7d1d927139be87d7474ac4e9d1cd2)

```
- id: 164
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x0000000000000000000000006bce15b789e537f3aba3c60cb183f0e8737f05ec]
- withDelegatecalls: [true]
- startBlock: 16688195
- endBlock: 16707395
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xa061b1a39bc913a61d79f06a1460a90db70cf205595d8dd4f563b964afbac2ce
```

<br>

### Aave Seatbelt report

[TBA]()

**The underlying Tenderly simulation infrastructure used by Seatbelt is having some problems, not allowing the report generation. We have double checked everything manually (including ad-hoc simulations) to verify that the proposal payload is correct.**

<br>

### Technical analysis

From a technical perspective, we have verified that the [proposal payload](https://optimistic.etherscan.io/address/0x6bce15b789e537f3aba3c60cb183f0e8737f05ec#code#F15#L1) does the following changes on Aave v3 Optimism, via the Aave cross-chain governance system:

1. WBTC:
  - Liquidation Bonus: **10% -> 9.4%**

2. sUSD:
  - Liquidation Bonus: **5% -> 5.4%**

The proposal payload corresponds to the specification on the governance forum, regarding the Optimism part.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:x: BGD reviewed the procedure followed to submit the proposal.
