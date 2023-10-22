# Proposal 348. Aave v3 Optimism - enable OP borrowing

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=348](https://app.aave.com/governance/proposal/?proposalId=348)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-op-risk-parameters-update-aave-v3-optimism-pool/14633](https://governance.aave.com/t/arfc-op-risk-parameters-update-aave-v3-optimism-pool/14633)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal enables OP as borrowable asset on Aave v3 Optimism, completing the updates started on proposal 337.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xef1625854fcd616f1293565a86915dd82982c369638107193e956ba39f2ecab9](https://etherscan.io/tx/0xef1625854fcd616f1293565a86915dd82982c369638107193e956ba39f2ecab9)

```
- id: 348
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x0000000000000000000000009c11f54ba3c44ed7945d2405c15060bcd209f53e]
- withDelegatecalls: [true]
- startBlock: 18378320
- endBlock: 18397520
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x06a8990a8b654dc91b27ca17cdfd38279aaa22e9900bfa122132578959118c26
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/348.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/348.md)

**Optimism**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/348_Optimism_39.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/348_Optimism_39.md)


<br>

### Technical analysis

The [proposal payload](https://optimistic.etherscan.io/address/0x9c11f54ba3c44ed7945d2405c15060bcd209f53e#code#F1#L13) correctly uses the BGD's Aave Config Engine of Aave v3 Optimism, for enabling OP as borrowable asset.

The payload is aligned with the description on the Aave governance forum and Snapshot.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
