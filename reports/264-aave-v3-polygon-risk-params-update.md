# Proposal 264. Aave v3 Polygon - CRV risk parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=264](https://app.aave.com/governance/proposal/?proposalId=264)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-update-crv-aave-v3-polygon-2023-06-20/13767](https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-update-crv-aave-v3-polygon-2023-06-20/13767)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal adjusts the LTV and Liquidation Threshold parameters of CRV on Aave v3 Polygon.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x6582d67e4451bf9b383b3b3b5d31e245250e82016fd0b6c912b650769ba0c664](https://etherscan.io/tx/0x6582d67e4451bf9b383b3b3b5d31e245250e82016fd0b6c912b650769ba0c664)

```
- id: 264
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000134c50556de1a83dd947c9460a58d8d60a289cea]
- withDelegatecalls: [true]
- startBlock: 17633857
- endBlock: 17653057
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x559ffffaa13a603d3f92b129aa04ff5c2a6ecb32b6b20c3e23aed073ccbf3bde
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/264.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/264.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://polygonscan.com/address/0x134c50556de1a83dd947c9460a58d8d60a289cea#code#F1#L13) does the following changes by interacting with the BGD Aave v3 Polygon Config Engine:

CRV
- LTV: 75% -> **70%**
- Liquidation Threshold: 80% -> **75%**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
