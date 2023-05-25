# Proposal 232. Aave v3 Ethereum - Add rETH to ETH-correlated e-mode

<br>


### Voting link

[https://app.aave.com/governance/proposal/?proposalId=232](https://app.aave.com/governance/proposal/?proposalId=232)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-activate-emode-for-reth-aave-ethereum-v3-pool/13034](https://governance.aave.com/t/arfc-activate-emode-for-reth-aave-ethereum-v3-pool/13034)

<br>

## BGD analysis

<br>

### Proposal types

:zap: emode

<br>

### Context

This proposal adds rETH to ETH-correlated eMode on Aave v3 Ethereum (eMode 1).


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x58416609ea33e5bb3daf5085aace902b0ea7ff8713aee3183e25f31fa25053b6](https://etherscan.io/tx/0x58416609ea33e5bb3daf5085aace902b0ea7ff8713aee3183e25f31fa25053b6)

```
- id: 232
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x301782f98846d15f57d1d202fba5acdecd336d0e]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17323163
- endBlock: 17342363
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x1128ef9ca9f89b3677e0b42b980fed6e4f298e1dfdf5b78e5023db368dad1139
```

<br>

### Aave Seatbelt reports

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/232.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/232.md)

<br>

### Technical analysis

The [proposal payload](https://etherscan.io/address/0x301782f98846d15f57d1d202fba5acdecd336d0e#code#F1#L13) simply interacts with the Aave v3 Ethereum Config Engine to add the rETH asset to eMode 1, ETH-correlated.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
