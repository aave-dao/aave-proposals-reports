# Proposal 95. Listing of LUSD on Aave v2 Ethereum

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=95](https://app.aave.com/governance/proposal/?proposalId=95)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-add-support-for-lusd-liquity/8443](https://governance.aave.com/t/arc-add-support-for-lusd-liquity/8443)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists the [LUSD asset](https://etherscan.io/address/0x5f98805A4E8be255a32880FDeC7F6728C6568bA0) into Aave v2 Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x3c45b73fd5d07e2ef21c705d812da492424079998ef8210303144df55d0930f0](https://etherscan.io/tx/0x3c45b73fd5d07e2ef21c705d812da492424079998ef8210303144df55d0930f0)

```
- id: 95
- creator: 0xf06016d822943c42e3cb7fc3a6a3b1889c1045f8
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xe0070f7a961dcb102e3d904a170613be3f3b37a9]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 15407941
- endBlock: 15427141
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xe4daadc3e2908d80c1f613d8c9afd20531f47163444bde175732556d3d3b5575
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/095.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/095.md)


<br>

### Technical analysis

This proposal lists LUSD into Aave V2 Ethereum by using the proposal payload on [https://etherscan.io/address/0xe0070f7a961dcb102e3d904a170613be3f3b37a9#code](https://etherscan.io/address/0xe0070f7a961dcb102e3d904a170613be3f3b37a9#code).

We have verified that the listing is consistent with the parameters defined on the governance forum and Snapshot.

A summary:
- A new oracle feed is properly configured for the asset.
- The asset is enabled to borrow, on both variable and stable modes.
- The asset is not enabled as collateral.
- The interest rate strategy configured follows same parameters as other stablecoins on the pool (DAI).
- Reserve factor: 10%

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
