# Proposal 141. Listing of OP on Aave v3 Optimism

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=141](https://app.aave.com/governance/proposal/?proposalId=141)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-add-op-as-collateral-to-aave-v3/9087](https://governance.aave.com/t/arc-add-op-as-collateral-to-aave-v3/9087)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

:link: :bridge_at_night: cross-chain execution

<br>

### Context

This proposal lists the [OP asset](https://optimistic.etherscan.io/address/0x4200000000000000000000000000000000000042) into Aave v3 Optimism, via a cross-chain governance action.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xcc9eb6e693cf7e45b04b43bb15f595cd43067b58277874672d4f21a131f6d127](https://etherscan.io/tx/0xcc9eb6e693cf7e45b04b43bb15f595cd43067b58277874672d4f21a131f6d127)

```
- id: 141
- creator: 0x3041ba32f451f5850c147805f5521ac206421623
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x0000000000000000000000006f76eedcb386fef8fc57bee9d3eb46147e488eef]
- withDelegatecalls: [true]
- startBlock: 16378773
- endBlock: 16397973
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x20f57c3ef4ee80ce54234133fe98d096adf40a60a982389bc3d3a258ed67bb44
```

<br>

### Aave Seatbelt report


**Ethereum report:**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/141.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/141.md)

**Optimism report:**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/141_optimism_2_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/141_optimism_2_0.md)



<br>

### Technical analysis

This proposal lists OP on Optimism, following the example and procedure present on [https://github.com/bgd-labs/aave-v3-crosschain-listing-template](https://github.com/bgd-labs/aave-v3-crosschain-listing-template).

We have verified that the listing is consistent with the parameters defined on the [governance forum] by Gauntlet (https://governance.aave.com/t/arc-add-op-as-collateral-to-aave-v3/9087/18).

A summary:
- A new oracle feed ([Chainlink OP/USD](https://optimistic.etherscan.io/address/0x0D276FC14719f9292D5C1eA2198673d1f4269246#readContract)) is properly configured for the asset.
- The asset is not enabled to borrow.
- The asset is enabled as collateral in isolation, with parameters as following:
  - LTV: 30%
  - Liquidation Threshold: 40%
  - Liquidation Bonus: 10%
- Supply cap: 20'000'000 OP.
- Debt ceiling: 2'000'000 USD.
- Reserve factor: 20%
- Liquidation protocol fee: 10%

In addition, we have checked that the implementation of the [OP token](https://optimistic.etherscan.io/address/0x4200000000000000000000000000000000000042#code) doesn't introduce any technical risk to the protocol. Certora has also applied their framework of ERC20 formal properties, not finding any meaningful risk [HERE](https://www.certora.com/erc20s/aave-listings/).



The proposal payload can be found on [https://optimistic.etherscan.io/address/0x6f76EeDCB386fef8FC57BEE9d3eb46147e488eEF#code](https://optimistic.etherscan.io/address/0x6f76EeDCB386fef8FC57BEE9d3eb46147e488eEF#code)

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
