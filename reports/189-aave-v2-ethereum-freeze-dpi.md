# Proposal 189. DPI freezing on Aave v2 Ethereum

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=189](https://app.aave.com/governance/proposal/?proposalId=189)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-add-dpi-to-v3-ethereum-and-freeze-on-v2-ethereum/12354](https://governance.aave.com/t/arfc-add-dpi-to-v3-ethereum-and-freeze-on-v2-ethereum/12354)

<br>

## BGD analysis

<br>

### Proposal types

:ice_cube: freeze-asset

<br>

### Context

The proposal freezes DPI on Aave v2 Ethereum, stopping new deposits and borrowings, but keeping all other dynamics (repayment, liquidation).

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x7cc2b3fc82dead9d3fb4250422ce7c7f218fe323179c0169898015295ec7b33d](https://etherscan.io/tx/0x7cc2b3fc82dead9d3fb4250422ce7c7f218fe323179c0169898015295ec7b33d)

```
- id: 189
- creator: 0xbc540e0729b732fb14afa240aa5a047ae9ba7df0
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x6fc2ac992cda41ed830cdffe16122f6136c60646]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16897495
- endBlock: 16916695
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xd4c1c21b50d76e454ec719e637734d1f5e3921a18c3c231ec2a92a32d9993fe3
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/189.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/189.md)


<br>

### Technical analysis

The [proposal payload](https://etherscan.io/address/0x6fc2ac992cda41ed830cdffe16122f6136c60646#code#F4#L1) simply interacts with the [PoolConfigurator](https://etherscan.io/address/0x311Bb771e4F8952E6Da169b425E7e92d6Ac45756) of Aave v2 Ethereum to freeze DPI by calling the `freezeReserve()` function.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
