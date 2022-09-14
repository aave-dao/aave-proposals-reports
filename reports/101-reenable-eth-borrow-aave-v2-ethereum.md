# Proposal 101. Re-enable ETH Borrowing on Aave v2 Ethereum

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=101](https://app.aave.com/governance/proposal/?proposalId=101)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-re-enabling-eth-borrowing-post-merge/9657](https://governance.aave.com/t/arc-re-enabling-eth-borrowing-post-merge/9657)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

:hammer: :ice_cube: reenable-borrow

<br>

### Context

This proposal re-enables ETH borrowing (via WETH) on Aave v2 Ethereum, previously halted by proposal 97 as cautionary measure pre-Merge.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xa5df5a5c8d3c3deba566d32c92592b127dec423ef645833568010a6cc67639bf](https://etherscan.io/tx/0xa5df5a5c8d3c3deba566d32c92592b127dec423ef645833568010a6cc67639bf)

```
- id: 101
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x311bb771e4f8952e6da169b425e7e92d6ac45756]
- values: [0]
- signatures: []
- calldatas: [0xeede87c1000000000000000000000000c02aaa39b223fe8d0a0e5c4f27ead9083c756cc20000000000000000000000000000000000000000000000000000000000000001]
- withDelegatecalls: [false]
- startBlock: 15529036
- endBlock: 15548236
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x1ad639a0fe12d46fdce998b69b9f9d9d13108baf13d35fea601f1017c3723364
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/101.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/101.md)


<br>

### Technical analysis

We have verified, that this proposal, as described on Snapshot and the Aave governance forum, does the following:
1. Call `enableBorrowingOnReserve()` for WETH on the [pool configurator of Aave v2 Ethereum](https://etherscan.io/address/0x311Bb771e4F8952E6Da169b425E7e92d6Ac45756).

As we have commented on the Aave governance forum, in terms of timing, we don't see any problem, as the Ethereum should have happened once this proposal (if passing) will be ready for execution.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: Payload encoded via multiple targets and calldatas, no delegatecall

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:x: BGD reviewed the procedure followed to submit the proposal.
