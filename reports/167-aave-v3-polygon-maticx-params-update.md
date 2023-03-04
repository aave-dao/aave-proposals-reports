# Proposal 167. Aave v3 Polygon - MATICX Risk parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=167](https://app.aave.com/governance/proposal/?proposalId=167)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-maticx-polygon-v3-upgrade/11555](https://governance.aave.com/t/arfc-maticx-polygon-v3-upgrade/11555)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal the risk parameters of MATICX on Aave v3 Polygon, including collateral configurations, caps, cap and interest rate strategy.
Additionally, MATICX is enabled for borrowing.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x51582eac1ddfef9bdc9f1f45a9e13b76be4094880724595fda41a0507ac0494a](https://etherscan.io/tx/0x51582eac1ddfef9bdc9f1f45a9e13b76be4094880724595fda41a0507ac0494a)

```
- id: 167
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x00000000000000000000000046a1b7d4a2920270c7eb2c2db4df2259a109bcb4]
- withDelegatecalls: [true]
- startBlock: 16741620
- endBlock: 16760820
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x49b18bdf919604d435b7a3736c5a9a728a96874783f5a50fab2ed4aa61f5fb6f
```

<br>

### Aave Seatbelt reports

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/167.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/167.md)


**Polygon**

[TBA](TBA)


<br>

### Technical analysis

From a technical perspective, we have verified that the proposal payload does the following changes on MATICX on Aave v3 Polygon:

- Enable the asset for borrowing.
- Supply cap changed to **8'600'000 MATICX**
- Borrow cap changed to **5'200'000 MATICX**
- Liquidation protocol fee changed to **10%**
- Collateral params changes:
  - LTV: 50 -> **58%**
  - Liquidation Threshold: 65% -> **67%**
- Interest rate strategy parameters:
  - Base variable borrow rate: **0.25%**
  - Optimal utilization: **45%**
  - Variable slope 1: **4%**
  - Variable slope 2: **150%**
  - Base stable rate offset: **2%**
  - Stable slope 1: **0.5%**
  - Stable slope 2: **150%**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
