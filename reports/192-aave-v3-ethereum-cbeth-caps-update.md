# Proposal 192. Aave v3 Ethereum - cbETH supply cap update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=192](https://app.aave.com/governance/proposal/?proposalId=192)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-increase-cbeth-supply-cap-03-26/12480](https://governance.aave.com/t/arfc-increase-cbeth-supply-cap-03-26/12480)

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

Transaction: [https://etherscan.io/tx/0xa0d1524b7bdd867efa29d05f87577eaff43b5decbf51eead5ffdd2607ef69150](https://etherscan.io/tx/0xa0d1524b7bdd867efa29d05f87577eaff43b5decbf51eead5ffdd2607ef69150)

```
- id: 192
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x25d9cda56174284d86ebbc28e7c99ce2e7a14c09]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16940297
- endBlock: 16959497
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x684825bca9aec1e56e63c1c5cbfcb322610f68d3a165342d307ed679d62c9be4
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/192.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/192.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x25d9cda56174284d86ebbc28e7c99ce2e7a14c09#code#F21#L1) correctly updates the supply cap of cbETH from 30'000 cbETH to **60'000 cbETH**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
