# Proposal 126. Aave v2 Polygon - Risk Parameter Updates

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=126](https://app.aave.com/governance/proposal/?proposalId=126)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-risk-parameter-recommendations-for-aave-v2-polygon-2022-11-25/10826](https://governance.aave.com/t/arc-risk-parameter-recommendations-for-aave-v2-polygon-2022-11-25/10826)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

:link: :bridge_at_night: cross-chain execution


<br>

### Context

This proposal is an update of risk parameters on Aave v2 Ethereum by Chaos Labs and Llama, applying more granular changes than the ones on [proposal 124](https://app.aave.com/governance/proposal/?proposalId=124).


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x4a80c7b20bfd8fb541a8316a5d7f3d221eafbe2ee6620d23a41e31717efe4980](https://etherscan.io/tx/0x4a80c7b20bfd8fb541a8316a5d7f3d221eafbe2ee6620d23a41e31717efe4980)

```
- id: 126
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000face5fafb0b61f77a67d239b3d1c94f08536db62]
- withDelegatecalls: [true]
- startBlock: 16068293
- endBlock: 16087493
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xdff78c5c3bbca49817d979701bb606c9779f290360755dd451d8e78c2f4444d0
```

<br>

### Aave Seatbelt report

**Ethereum report:**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/126.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/126.md)

**Polygon report:**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/126_fx_8_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/126_fx_8_0.md)

(There are some inconsistencies on the storage changes, due to inter-dependency with proposal 124, to be fixed soon)

<br>

### Technical analysis

Like on every Aave cross-chain proposal, this one follows the procedure defined on [https://github.com/bgd-labs/aave-v3-crosschain-listing-template](https://github.com/bgd-labs/aave-v3-crosschain-listing-template). This means that after execution on Ethereum, the proposal payload will be queued on the Polygon side of the cross-chain infrastructure and, after the timelock there, will be open for execution.

From a technical perspective, we have verified that the proposal payload does the following changes on Aave v2 Polygon, by interacting with the [Aave v2 Polygon Configurator](https://polygonscan.com/address/0x26db2B833021583566323E3b8985999981b9F1F3):

- BAL
  - **Freeze** (already frozen by 124, so no extra effect)

- CRV
  - **Unfreeze**
  - **Disable borrowing**

- GHST
  - **Freeze** (already frozen by 124, so no extra effect)

- LINK
  - **Unfreeze**
  - **Disable borrowing**

- SUSHI
  - **Freeze** (already frozen by 124, so no extra effect)

- DPI (as described on the governance forum, but not as reflected in the table on the AIP)
  - **Unfreeze** (already frozen by 124, so no extra effect)
  - **Disable borrowing** (already disabled, so no extra effect)


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
