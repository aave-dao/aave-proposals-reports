# Proposal 188. Aave v3 Ethereum - wstETH, rETH caps updates

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=188](https://app.aave.com/governance/proposal/?proposalId=188)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-gauntlet-recommendations-for-wsteth-and-reth-on-eth-v3/12349](https://governance.aave.com/t/arc-gauntlet-recommendations-for-wsteth-and-reth-on-eth-v3/12349)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the borrow caps of wstETH and rETH on Aave v3 Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xc70bbe74c4950b6d52bc12b3e803baeb7611a6f271f46dcc806b2d34fc4ecccd](https://etherscan.io/tx/0xc70bbe74c4950b6d52bc12b3e803baeb7611a6f271f46dcc806b2d34fc4ecccd)

```
- id: 188
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xf4d1352b3e9e99fca6aa20f62fe95192a26c9527]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16894506
- endBlock: 16913706
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x11a1f4443dd21c76734e1302c889815bab750e28f6c8f69d110596f36270ca36
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/feat/188/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/188.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/feat/188/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/188.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xf4d1352b3e9e99fca6aa20f62fe95192a26c9527#code#F21#L1) correctly updates the borrow cap of wstETH to **6'000 wstETH** and the one of rETH to **2'400 rETH**.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
