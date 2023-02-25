# Proposal 161. Aave v3 Ethereum - update cbETH supply cap

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=161](https://app.aave.com/governance/proposal/?proposalId=161)

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

This proposal increases the supply cap of cbETH on Aave v3 Ethereum.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x2e464c72a3a106955bc4d0356e30d640ddd6dcf8785ab093da040d24eec3360c](https://etherscan.io/tx/0x2e464c72a3a106955bc4d0356e30d640ddd6dcf8785ab093da040d24eec3360c)

```
- id: 161
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x4e3728f85818780451e1f44fa3689c85a1229801]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16678210
- endBlock: 16697410
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xf7ac3c7b7252b6ca6ee17efb10f9f31c9f22bfb737573085b3e57d89456be123
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/161.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/161.md)

<br>

### Technical analysis

The [proposal payload](https://etherscan.io/address/0x4e3728f85818780451e1f44fa3689c85a1229801#code#F15#L1) simply interacts with the [PoolConfigurator](https://etherscan.io/address/0x64b761D848206f447Fe2dd461b0c635Ec39EbB27#code) of Aave v3 Ethereum to update the supply cap of cbETH from 10'000 cbETH to 20'000 cbETH by calling the `setSupplyCap()` function.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
