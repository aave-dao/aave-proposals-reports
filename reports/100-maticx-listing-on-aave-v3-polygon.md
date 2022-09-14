# Proposal 100. Listing of MATICX on Aave v3 Polygon

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=100](https://app.aave.com/governance/proposal/?proposalId=100)

<br>

### Governance forum discussion

[https://governance.aave.com/t/proposal-to-add-maticx-to-aave-v3-polygon-market/7995](https://governance.aave.com/t/proposal-to-add-maticx-to-aave-v3-polygon-market/7995)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

:link: :bridge_at_night: cross-chain execution

<br>

### Context

This proposal lists the [MATICX asset](https://polygonscan.com/address/0xfa68FB4628DFF1028CFEc22b4162FCcd0d45efb6) into Aave v3 Polygon, via a cross-chain governance action.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x504bea849c85412ec3208ad443a09f945542cc056f061a93f32d47e2c3b97e68](https://etherscan.io/tx/0x504bea849c85412ec3208ad443a09f945542cc056f061a93f32d47e2c3b97e68)

```
- id: 100
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000d417d07c20e31f6e129fa68182054b641fbec8bd]
- withDelegatecalls: [true]
- startBlock: 15528369
- endBlock: 15547569
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x0a387fa966f5616423bea53801a843496b1eac5cab5e6bc9426c0958e6496e77
```

<br>

### Aave Seatbelt report


**Ethereum report:**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/100.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/100.md)

**Polygon report:**

**IMPORTANT**. We are aware that Seatbelt is currently failing, but that is due to the dependency with Proposal 99 (stMATIC) creating eMode 2. As soon as 99 will be executed, Seatbelt will show proposal 100 as passing.

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/100_fx_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/100_fx_0.md)



<br>

### Technical analysis

This proposal lists MATICX on Polygon, following the example and procedure present on [https://github.com/bgd-labs/aave-v3-crosschain-listing-template](https://github.com/bgd-labs/aave-v3-crosschain-listing-template).

We have verified that the listing is consistent with the parameters defined on the governance forum and Snapshot.

A summary:
- A new oracle feed is properly configured for the asset. We have confirmed that this feed is a Chainlink calculated feed, which same as stMATIC, gives good assurances.
- The asset is not enabled to borrow.
- The asset is enabled as collateral, with parameters as following:
  - LTV: 50%
  - Liquidation Threshold: 65%
  - Liquidation Bonus: 10%
- Supply cap: 6'000'000 MATICX.
- eMode category: 2, MATIC-correlated assets.
- Reserve factor: 20%
- Liquidation protocol fee: 20%

**IMPORTANT** For this proposal to correctly pass, it is assumed that [Proposal 99 to list stMATIC](https://app.aave.com/governance/proposal/99/) is already executed, as the eMode 2 set is created on that proposal. The proposal's vote has passed before before this 100 has been created, which we think is enough requirement to assume execution.

The proposal payload can be found on [https://polygonscan.com/address/0xD417d07c20e31F6e129fa68182054B641FbEC8Bd#code](https://polygonscan.com/address/0xD417d07c20e31F6e129fa68182054B641FbEC8Bd#code)

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
