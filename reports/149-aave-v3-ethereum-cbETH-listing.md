# Proposal 149. Aave v3 Ethereum - listing of cbETH

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=149](https://app.aave.com/governance/proposal/?proposalId=149)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-add-support-for-cbeth/10425](https://governance.aave.com/t/arc-add-support-for-cbeth/10425)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists cbETH (Coinbase Wrapped Staked ETH) on the Aave v3 Ethereum pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xb256802f9d5372ff726db0ae9dcfecc03258baef46fb290bf7f02951e1aafcc2](https://etherscan.io/tx/0xb256802f9d5372ff726db0ae9dcfecc03258baef46fb290bf7f02951e1aafcc2)

```
- id: 149
- creator: 0x62a43123fe71f9764f26554b3f5017627996816a
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xd91d1331db4f436daf47ec9dd86decb8eef946b4]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16543915
- endBlock: 16563115
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x05097b8a0818a75c1db7d54dfd0299581cac0218a058017acb4726f7cc49657e
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/149.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/149.md)


<br>

### Technical analysis

The [proposal payload](https://etherscan.io/address/0xd91d1331db4f436daf47ec9dd86decb8eef946b4#code) follows the new approach for listings, using the [Aave V3 listing engine contract](https://etherscan.io/address/0xC51e6E38d406F98049622Ca54a6096a23826B426#code), containing logic to expose a simple interface for listings, and do proper validations.

We have verified this payload respects the interface required by the v3 listing engine and effectively configures the cbETH listing with the following initial parameters:

- The asset is enabled for borrowing and the interest rate strategy follows the parameters on the forum:
  - Base variable borrow: 0
  - Variable borrow slope 1: 7%
  - Variable borrow slope 2: 300%
  - Optimal point: 45%
- LTV: 67%
- Liquidation Threshold: 74%
- Liquidation Bonus: 7.5%
- Reserve Factor: 15%
- Liquidation protocol fee: 10%
- Supply cap: 10'000 cbETH
- Borrow cap: 1'200 cbETH
- No eMode category
- No isolation mode
- Flashlonable
- Not enabled for borrowing on isolation

We have deployed [the oracle adapter](https://etherscan.io/address/0x5f4d15d761528c57a5C30c43c1DAb26Fc5452731#code) connected to the asset, and verified it works correctly, by using the underlying ETH/USD and cbETH/ETH Chainlink price feeds.

The initial configuration is completely aligned with the description on the Aave governance forum.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
