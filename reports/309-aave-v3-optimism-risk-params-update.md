# Proposal 309. Aave v3 Optimism - Risk parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=309](https://app.aave.com/governance/proposal/?proposalId=309)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-aave-v3-optimism-2023-08-13/14466](https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-aave-v3-optimism-2023-08-13/14466)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates multiple risk parameters on Aave v3 Optimism.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x26bc124a4cdb418cdc8f5c7acdf5b1c127cd66bd535c93f7befa6145587d1f3d](https://etherscan.io/tx/0x26bc124a4cdb418cdc8f5c7acdf5b1c127cd66bd535c93f7befa6145587d1f3d)

```
- id: 309
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000134c50556de1a83dd947c9460a58d8d60a289cea]
- withDelegatecalls: [true]
- startBlock: 18030309
- endBlock: 18049509
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xad315f6890989f8d141365f2d542e2639bdae782d12126532b469a79e9cb21be
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/309.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/309.md)

**Optimism**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/309_Optimism_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/309_Optimism_pending_0.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://optimistic.etherscan.io/address/0x134c50556de1a83dd947c9460a58d8d60a289cea#code#F1#L13) updates the following parameters on Aave v3 Optimism, by using the BGD Config Engine:

WBTC

- Liquidation Bonus: 8.5% -> **7.5%**

wstETH

- LTV: 70% -> **71%**
- Liquidation Threshold: 79% -> **80%**

The proposal is consistent with the discussions on the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
