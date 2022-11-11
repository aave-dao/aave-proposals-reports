# Proposal 116. Listing of OP on Aave v3 Optimism

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=116](https://app.aave.com/governance/proposal/?proposalId=116)

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

Transaction: [https://etherscan.io/tx/0xf7afe2569894da136fc5d011d2eb8e079f3666412220268b30f492211e164f26](https://etherscan.io/tx/0xf7afe2569894da136fc5d011d2eb8e079f3666412220268b30f492211e164f26)

```
- id: 116
- creator: 0x3041ba32f451f5850c147805f5521ac206421623
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x0000000000000000000000005f5c02875a8e9b5a26fbd09040abcfdeb2aa6711]
- withDelegatecalls: [true]
- startBlock: 15951230
- endBlock: 15970430
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x7ecafb3b0b7e418336cccb0c82b3e25944011bf11e41f8dc541841da073fe4f1
```

<br>

### Aave Seatbelt report


**Ethereum report:**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/116.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/116.md)

**Optimism report:**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/64ee41eabf8dbec1a7727316db27332faf07e2ad/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/116_optimism_0_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/64ee41eabf8dbec1a7727316db27332faf07e2ad/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/116_optimism_0_0.md)



<br>

### Technical analysis

This proposal lists OP on Optimism, following the example and procedure present on [https://github.com/bgd-labs/aave-v3-crosschain-listing-template](https://github.com/bgd-labs/aave-v3-crosschain-listing-template).

We have verified that the listing is consistent with the parameters defined on the [governance forum](https://governance.aave.com/t/arc-add-op-as-collateral-to-aave-v3/9087/7).

A summary:
- A new oracle feed ([Chainlink OP/USD](https://optimistic.etherscan.io/address/0x0D276FC14719f9292D5C1eA2198673d1f4269246#readContract)) is properly configured for the asset.
- The asset is not enabled to borrow.
- The asset is enabled as collateral, with parameters as following:
  - LTV: 50%
  - Liquidation Threshold: 65%
  - Liquidation Bonus: 10%
- Supply cap: 40'000'000 OP.
- Reserve factor: 20%
- Liquidation protocol fee: 10%

In addition, we have checked that the implementation of the [OP token](https://optimistic.etherscan.io/address/0x4200000000000000000000000000000000000042#code) doesn't introduce any technical risk to the protocol. Certora has also applied their framework of ERC20 formal properties, not finding any meaningful risk [HERE](https://www.certora.com/erc20s/aave-listings/).



The proposal payload can be found on [https://optimistic.etherscan.io/address/0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711#code](https://optimistic.etherscan.io/address/0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711#code)

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
