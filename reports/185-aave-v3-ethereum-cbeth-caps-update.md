# Proposal 185. Aave v3 Ethereum - cbETH caps update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=185](https://app.aave.com/governance/proposal/?proposalId=185)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-increase-supply-cap-for-cbeth-aave-ethereum-v3-20230317/12334](https://governance.aave.com/t/arfc-increase-supply-cap-for-cbeth-aave-ethereum-v3-20230317/12334)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the supply cap of cbETH on Aave v3 Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x140fe50fd779af0b04827337704c1f0cad9de2478b60a070acce448e6e3f9d06](https://etherscan.io/tx/0x140fe50fd779af0b04827337704c1f0cad9de2478b60a070acce448e6e3f9d06)

```
- id: 185
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xb6e50599ba78c6ccd40df8b903e3d76ae68dcc83]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16875307
- endBlock: 16894507
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x2426029bb07fa6f4c7c60d427f63abbca45cf592822b01c3f7910f3735560c2b
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/185.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/185.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xb6e50599ba78c6ccd40df8b903e3d76ae68dcc83#code#F15#L1) correctly updates the supply cap of cbETH from 20'000 cbETH to **30'000 cbETH**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
