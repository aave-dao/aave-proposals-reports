# Proposal 304. Treasury Management - Chaos Labs scope amendment

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=304](https://app.aave.com/governance/proposal/?proposalId=304)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-scope-and-compensation-amendment/14407](https://governance.aave.com/t/arfc-chaos-labs-scope-and-compensation-amendment/14407)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposal approves an extension of scope and budget for Chaos Labs, for coverage of Aave v2, v3 and GHO, until November 7th.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x3756e14cd7475d778c8b75fd41f84c62c5335c3adec7604b8856206c6799bdfb](https://etherscan.io/tx/0x3756e14cd7475d778c8b75fd41f84c62c5335c3adec7604b8856206c6799bdfb)

```
- id: 304
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xea6d8cfaa0c3d018a8adb7431081458317adf592]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17983598
- endBlock: 18002798
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x3b8798b851c0ec0c8c89aab4d6ed05ab5253d5e3c479f19439d1fe23496f4098
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/304.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/304.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xea6d8cfaa0c3d018a8adb7431081458317adf592#code#F1#L16) does the following:

1. Migrates ~400'000 of USDT from Aave v2 Ethereum to Aave v3 Ethereum.

2. Creates an stream of ~400'000 aUSDT v3 from the Aave Ethereum Collector to the address defined as [CHAOS_LABS_TREASURY](https://etherscan.io/address/0xbC540e0729B732fb14afA240aA5A047aE9ba7dF0), with a duration of 77 days and starting at the time of proposal execution.

We have confirmed the amount and duration is consistent with what is defined on the Aave governance forum, Snapshot and AIP.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
