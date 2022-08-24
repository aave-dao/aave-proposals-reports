# Proposal 93. Listing of MAI (miMATIC) on Aave v3 Polygon

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=93](https://app.aave.com/governance/proposal/?proposalId=93)

<br>

### Governance forum discussion

[https://governance.aave.com/t/add-mai-on-aave-v3/7630](https://governance.aave.com/t/add-mai-on-aave-v3/7630)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

:link: :bridge_at_night: cross-chain execution

<br>

### Context

This proposal lists the [MAI (miMATIC) asset](https://polygonscan.com/address/0xa3Fa99A148fA48D14Ed51d610c367C61876997F1) into Aave v3 Polygon, via a cross-chain governance action.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x38241b647138bbead36061d1e53aec415c57c85784b286ede534e4a971c9881a](https://etherscan.io/tx/0x38241b647138bbead36061d1e53aec415c57c85784b286ede534e4a971c9881a)

```
- id: 93
- creator: 0x985a29e88e75394dbdae41a269409f701ccf6a43
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x00000000000000000000000083fba23163662149b33dbc05cf1312df6dcba72b]
- withDelegatecalls: [true]
- startBlock: 15396902
- endBlock: 15416102
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xf6e50d5a3f824f5ab4ffa15fb79f4fa1871b8bf7af9e9b32c1aaaa9ea633006d
```

<br>

### Aave Seatbelt report

Aave Seatbelt supports now cross-chain governance proposals as first-class citizen of the verification procedure, generating one report for the Ethereum side of the proposal, and another for the final action happening on the execution chain, Polygon in this case.

**Ethereum report:**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/093.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/093.md)

**Polygon report:**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/093_fx_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/093_fx_0.md)

IMPORTANT. Cross-chain simulation seems to still have some problems on the infrastructure side (Tenderly), and we have noticed some incorrect reporting of storage changes on addresses where it is technically impossible (EOAs).



<br>

### Technical analysis

This proposal lists MAI on Polygon, following the example and procedure present on [https://github.com/bgd-labs/aave-v3-crosschain-listing-template](https://github.com/bgd-labs/aave-v3-crosschain-listing-template).
BGD has supported the proposer on the technical aspects of the proposal payload, given that is the first time a listing happens cross-chain using this procedure.

We have verified that the listing is consistent with the parameters defined on the governance forum and Snapshot, with those not defined just following the same approach as similar-nature assets, already listed.

A summary:
- A new oracle feed is properly configured for the asset.
- The asset is enabled to borrow, on variable mode only. It is not borrowable against other assets in isolation.
- Isolated as collateral, with a debt ceiling of 2'000'000 USD. The collateral parameters in isolation are:
  - LTV: 75%
  - Liquidation Threshold: 80%
  - Liquidation Bonus: 5%
- Supply cap: 100'000'000 MAI.
- eMode category: 1, USD-correlated assets (stablecoins).
- Reserve factor: 10%
- Liquidation protocol fee: 10%

The proposal payload can be found on [https://polygonscan.com/address/0x83fba23163662149b33dbc05cf1312df6dcba72b#code](https://polygonscan.com/address/0x83fba23163662149b33dbc05cf1312df6dcba72b#code)

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
