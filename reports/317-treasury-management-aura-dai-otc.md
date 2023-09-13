# Proposal 317. Treasury Management - swap aDAI from treasury to AURA

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=317](https://app.aave.com/governance/proposal/?proposalId=317)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-treasury-management-acquire-aura/14683](https://governance.aave.com/t/arfc-treasury-management-acquire-aura/14683)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposal executes an OTC swap with Olympus DAO, of DAI from the Aave Ethereum Collector to AURA.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x627a677a65368cafde8831791eb40b6b3bb57e47da2c1f779bba36bef33177ca](https://etherscan.io/tx/0x627a677a65368cafde8831791eb40b6b3bb57e47da2c1f779bba36bef33177ca)

```
- id: 317
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xdfee3ec490caabf760f77b39652e4208a5848971]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 18099226
- endBlock: 18118426
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xa8fae12f14e52f4f19f4f008bfc67ec6ee7d22c5b5ee50b5a12063d215a9325f
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/317.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/317.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xdfee3ec490caabf760f77b39652e4208a5848971#code#F1#L15) does the following:

1. Transfer from the [Olympus DAO](https://etherscan.io/address/0x245cc372C84B3645Bf0Ffe6538620B04a217988B) 443'674 AURA tokens, to the Aave Ethereum Collector.
This will depend on the counterparty having given approval in advance to the Aave Governance Level 1 Executor (Short Executor).

2. Withdraw 420'159 aDAI from the Aave Ethereum Collector.

3. Redeem DAI from aDAI.

4. Transfer the DAI to the Olympus DAO address.

The proposal is consistent with the description in the forum and Snapshot.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
