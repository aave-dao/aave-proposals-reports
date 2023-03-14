# Proposal 173. Aave v3 Ethereum - update of cbETH supply cap

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=173](https://app.aave.com/governance/proposal/?proposalId=173)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-increase-supply-cap-for-cbeth-aave-ethereum-v3/11869](https://governance.aave.com/t/arfc-increase-supply-cap-for-cbeth-aave-ethereum-v3/11869)

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

Transaction: [https://etherscan.io/tx/0x2ac1a8930563b2268235b05cffb6a0f84ab3abd81a5c6e5e23b52d6e63c60d67](https://etherscan.io/tx/0x2ac1a8930563b2268235b05cffb6a0f84ab3abd81a5c6e5e23b52d6e63c60d67)

```
- id: 173
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xb6e50599ba78c6ccd40df8b903e3d76ae68dcc83]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16784382
- endBlock: 16803582
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x4f14b29139a93f1169afd329f5f7b9f5e8d8e55a252747c18ad50b23e9d1e249
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/173.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/173.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xb6e50599ba78c6ccd40df8b903e3d76ae68dcc83#code#F15#L1) only updates the cbETH supply cap from 20'000 cbETH to 30'000 cbETH.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
