# Proposal 184. Aave v3 Ethereum - add cbETH to ETH-correlated eMode

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=184](https://app.aave.com/governance/proposal/?proposalId=184)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-activate-emode-for-cbeth-aave-ethereum-v3/12074](https://governance.aave.com/t/arfc-activate-emode-for-cbeth-aave-ethereum-v3/12074)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal adds cbETH to ETH-correlated eMode on Aave v3 Ethereum (eMode 1).


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x261d1ff732221c447d962057f634a799d61773c873db501b7c54838b2f6e91ea](https://etherscan.io/tx/0x261d1ff732221c447d962057f634a799d61773c873db501b7c54838b2f6e91ea)

```
- id: 184
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x2b6de4f5a2a78f35d65d0d03bf4f12ffb2a26cbc]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16856445
- endBlock: 16875645
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x8c43863eb45efe9d794f07cf717a3f71d8fc315f693d42dff0f681e839d1419d
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/184.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/184.md)

<br>

### Technical analysis

The [proposal payload](https://etherscan.io/address/0x2b6de4f5a2a78f35d65d0d03bf4f12ffb2a26cbc#code#F15#L1) simply interacts with the [PoolConfigurator](https://etherscan.io/address/0x64b761D848206f447Fe2dd461b0c635Ec39EbB27#code) of Aave v3 Ethereum to add the cbETH assets to eMode 1, ETH-correlated.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
