# Proposal 350. Treasury Management - Fund Aave Companies for events organization 2023
<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=350](https://app.aave.com/governance/proposal/?proposalId=350)

<br>

### Governance forum discussion

[https://governance.aave.com/t/temp-check-aave-events-sponsorship-budget/14953](https://governance.aave.com/t/temp-check-aave-events-sponsorship-budget/14953)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposals releases 550'000 GHO to Aave Companies, for events organization during the remainder of 2023.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xcf244b554f17bf3ff01cc8726db5223260d1582666fa2f48b14f5233743a5bfc](https://etherscan.io/tx/0xcf244b554f17bf3ff01cc8726db5223260d1582666fa2f48b14f5233743a5bfc)

```
- id: 350
- creator: 0x391048fde157d2c3ddd066b8411e8e73439ed24d
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xfa9af30481942a31e6ae47f199c6c2a3978b5c33]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 18411799
- endBlock: 18430999
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xe8e7eaeb85300d528186683514e457815501c0e6b10296f3d0b6c90f06d6c376
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/350.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/350.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xfa9af30481942a31e6ae47f199c6c2a3978b5c33#code#F1#L14) properly releases 550'000 GHO from the Aave Ethereum Collector to the address defined as `RECEIVER`.

The proposal is consistent with Snapshot and governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
