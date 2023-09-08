# Proposal 313. Treasury Management - SigmaP scope amendment

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=313](https://app.aave.com/governance/proposal/?proposalId=313)

<br>

### Governance forum discussion

[https://governance.aave.com/t/bgd-sigma-prime-audit-budget-extension/14357](https://governance.aave.com/t/bgd-sigma-prime-audit-budget-extension/14357)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposal approves a payment of 162'000 aUSDT to SigmaP, to cover the cost audit of multiple projects: re-review of Aave Governance v3, a.DI and the GSM (Gho Stability Module).


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x5fc4fcc1ec068a5a075cd39727d5e2f8a1ed6d4f3c70aea4456194745c891d8d](https://etherscan.io/tx/0x5fc4fcc1ec068a5a075cd39727d5e2f8a1ed6d4f3c70aea4456194745c891d8d)

```
- id: 313
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x2ad4d4c989c4808439434cb556e1be1c55105aaf]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 18075587
- endBlock: 18094787
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x7e49177f1b176b8711a9098d594ff1b63e7435d769bb7f46ce62221689952af9
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/313.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/313.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x2ad4d4c989c4808439434cb556e1be1c55105aaf#code#F1#L14) properly transfers 162'000 aUSDT from the Aave v3 Collector to the address defined as [SIGP](https://etherscan.io/address/0x014D706F8C893166Da0C6C3343fF9359D1C08FA3).

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
