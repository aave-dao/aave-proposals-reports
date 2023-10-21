# Proposal 347. Treasury Management - GHO acquisition

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=347](https://app.aave.com/governance/proposal/?proposalId=347)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-treasury-management-gho-funding/14887/10](https://governance.aave.com/t/arfc-treasury-management-gho-funding/14887/10)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposal seeks to acquire approximately 1'600'000 GHO, by swapping partial Aave Collector's holdings of DAI, USDT, TUSD and BUSD.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xb1fde7c824c81b9e09e2bad17c4b1608ec0c1f7b13c969ef60a1dad768373992](https://etherscan.io/tx/0xb1fde7c824c81b9e09e2bad17c4b1608ec0c1f7b13c969ef60a1dad768373992)

```
- id: 347
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x121fe3fc3f617ace9730203d2e27177131c4315e]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 18377283
- endBlock: 18396483
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xe72061751d8a7381ccc67e9946e8acffa3f63dfa54b5f66ef58a29444cfa9b95
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/347.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/347.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x121fe3fc3f617ace9730203d2e27177131c4315e#code#F1#L31) does the following:
1. For those assets held in aToken on the Collector, it redeems them first.
2. Afterwards, they are transferred to the AaveSwapper smart contract, used previously in multiple proposals, integrated with CowSwap and Milkman.
3. Creates one buy order of GHO per sold asset, by calling `swap()` on the AaveSwapper.


The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
