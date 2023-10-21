# Proposal 346. Treasury Management - Addition of TokenLogic to Orbit

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=346](https://app.aave.com/governance/proposal/?proposalId=346)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-tokenlogic-hohmann-transfer/15051](https://governance.aave.com/t/arfc-tokenlogic-hohmann-transfer/15051)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposal includes TokenLogic into the Orbit delegate platform program, transitioned to the Aave DAO on Aave proposal 332.

In practise, it will create a of 90-days 15'000 GHO stream from the Aave Collector TokenLogic.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xa09ee9ddda93fa2567ad967b8e049129e860f28e20180fcfa00eb8e1face30b0](https://etherscan.io/tx/0xa09ee9ddda93fa2567ad967b8e049129e860f28e20180fcfa00eb8e1face30b0)

```
- id: 346
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xd446384e77b1386da0b53f3fbfc7e3e55552a89e]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 18376535
- endBlock: 18395735
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xb78fdcdffb1075e3b5c70b8a8c958685321ccd93f4263a40c70d3b92f47e96c9
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/346.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/346.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xd446384e77b1386da0b53f3fbfc7e3e55552a89e#code#F1#L13) properly creates five 90-day GHO stream from the Aave Collector to the address denominated as `TOKEN_LOGIC`.


The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
