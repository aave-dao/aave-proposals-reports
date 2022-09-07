# Proposal 99. Listing of stMATIC on Aave v3 Polygon

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=99](https://app.aave.com/governance/proposal/?proposalId=99)

<br>

### Governance forum discussion

[https://governance.aave.com/t/proposal-add-support-for-stmatic-lido/7677](https://governance.aave.com/t/proposal-add-support-for-stmatic-lido/7677)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

:link: :bridge_at_night: cross-chain execution

<br>

### Context

This proposal lists the [stMATIC asset](https://polygonscan.com/address/0x3A58a54C066FdC0f2D55FC9C89F0415C92eBf3C4) into Aave v3 Polygon, via a cross-chain governance action.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x55b01e8f8c2a8f3298e3e556ab897c991e46e0e62b8908820a9ccd09d278e627](https://etherscan.io/tx/0x55b01e8f8c2a8f3298e3e556ab897c991e46e0e62b8908820a9ccd09d278e627)

```
- id: 99
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000c730008c64783a283988b0fa3b5ee6b6f997922a]
- withDelegatecalls: [true]
- startBlock: 15486006
- endBlock: 15505206
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x344d3181f08b3186228b93bac0005a3a961238164b8b06cbb5f0428a9180b8a7
```

<br>

### Aave Seatbelt report


**Ethereum report:**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/099.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/099.md)

**Polygon report:**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/099_fx_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/099_fx_0.md)



<br>

### Technical analysis

This proposal lists stMATIC on Polygon, following the example and procedure present on [https://github.com/bgd-labs/aave-v3-crosschain-listing-template](https://github.com/bgd-labs/aave-v3-crosschain-listing-template).

We have verified that the listing is consistent with the parameters defined on the governance forum and Snapshot.

A summary:
- A new oracle feed is properly configured for the asset. During our verification process, we have place a lot of emphasis on the review of this component, given the activation of eMode between stMATIC and WMATIC. The [stMATIC/USD Chainlink feed](https://polygonscan.com/address/0x97371dF4492605486e23Da797fA68e55Fc38a13f#code) is a Chainlink calculated feed, meaning that its update depends on a previous update on the MATIC/USD price feed on-chain. This removes any potential risk of synchronization of updates.
- The asset is not enabled to borrow.
- The asset is enabled as collateral, with parameters as following:
  - LTV: 50%
  - Liquidation Threshold: 65%
  - Liquidation Bonus: 10%
- Supply cap: 7'500'000 stMATIC.
- eMode category: 2, MATIC-correlated assets (new eMode).
- Reserve factor: 20%
- Liquidation protocol fee: 20%

In addition to the changes for stMATIC, we have verified that the proposal creates a new eMode: 2, for MATIC-correlated assets.
On this eMode, both stMATIC and WMATIC are included, as expected.

The proposal payload can be found on [https://polygonscan.com/address/0xc730008C64783a283988b0fA3b5eE6b6F997922A#code](https://polygonscan.com/address/0xc730008C64783a283988b0fA3b5eE6b6F997922A#code)

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
