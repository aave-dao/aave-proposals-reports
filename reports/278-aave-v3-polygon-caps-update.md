# Proposal 278 (repetition of 276). Aave v3 Polygon - MATICx supply cap update

<br>


### Voting link

[https://app.aave.com/governance/proposal/?proposalId=278](https://app.aave.com/governance/proposal/?proposalId=278)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-polygon-supply-cap-update-07-07-2023/13928](https://governance.aave.com/t/arfc-polygon-supply-cap-update-07-07-2023/13928)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the supply cap of MATICx on Aave v3 Polygon.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xf46de5e85203d0043277aa9305892633b77f361a30c18b602a1c153596abf6c6](https://etherscan.io/tx/0xf46de5e85203d0043277aa9305892633b77f361a30c18b602a1c153596abf6c6)

```
- id: 278
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x0000000000000000000000007afc6e6f5f009016da501f40a2ff96b3fa7e2c09]
- withDelegatecalls: [true]
- startBlock: 17778056
- endBlock: 17797256
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xdc2654339761e78195b693d8d90ee96531d71c9c1236612d94a22c62554e3a92
```

<br>

### Aave Seatbelt reports

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/278.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/278.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/278_Polygon_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/278_Polygon_pending_0.md)

<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Polygon.

From a technical perspective, we have verified the [proposal payload](https://polygonscan.com/address/0x7afc6e6f5f009016da501f40a2ff96b3fa7e2c09#code#F1#L13) correctly uses the BGD's Aave Config Engine of Aave v3 Polygon, in this case, to update the supply cap of MATICx the following way:
- Supply cap: 38'000'000 MATICx -> **50'600'000 MATICx**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
