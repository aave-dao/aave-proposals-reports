# Proposal 263. Gas rebate for delegates

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=263](https://app.aave.com/governance/proposal/?proposalId=263)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-gas-rebate-for-recognized-delegates/13290](https://governance.aave.com/t/arfc-gas-rebate-for-recognized-delegates/13290)

<br>

## BGD analysis

<br>

### Proposal types

:money_with_wings: funds-release

<br>

### Context

This proposal transfers ~3 WETH from the Aave Collector to a number of recognized governance delegates, to cover for past gas cost expenses.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x67bf029efb51617b3c0b21c2e14ea63c6bcf1c9184812c126cea4b549f991c31](https://etherscan.io/tx/0x67bf029efb51617b3c0b21c2e14ea63c6bcf1c9184812c126cea4b549f991c31)

```
- id: 263
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x5a1c6e2c7e7b309e6e39fdcd88d6d96e783cf5ee]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17626488
- endBlock: 17645688
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xb07c4d2d2bdfae564b3c57dc209cf42e77d086e17f9cd362929b3080bf40c83c
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/263.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/263.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x5a1c6e2c7e7b309e6e39fdcd88d6d96e783cf5ee#code) effectively transfers approximately 3 WETH to 8 delegates (ACI split into 2 in the list of 9), by properly interacting with the Aave Ethereum Collector.

The proposal payload is consistent with [Snapshot](https://snapshot.org/#/aave.eth/proposal/0xff11b348c1e8df41555d7579c7785942378bcf09ff1d9ca97af1d86b2b124beb) and the forum description.



<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
