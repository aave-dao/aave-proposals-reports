# Proposal 301. Aave v3 Polygon - MATICx supply cap update

<br>


### Voting link

[https://app.aave.com/governance/proposal/?proposalId=301](https://app.aave.com/governance/proposal/?proposalId=301)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-increase-maticx-supply-cap/14341](https://governance.aave.com/t/arfc-increase-maticx-supply-cap/14341)

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

Transaction: [https://etherscan.io/tx/0x31c9957fcf88a7be925392c8a1aaa95529ea2c8c64a160a17f911a929f2bd447](https://etherscan.io/tx/0x31c9957fcf88a7be925392c8a1aaa95529ea2c8c64a160a17f911a929f2bd447)

```
- id: 301
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000f8ad3689e88cfec0afa82b65681336140574dd69]
- withDelegatecalls: [true]
- startBlock: 17930118
- endBlock: 17949318
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xcf4879103e3d98e72aac58a16f5eae53e9336b419379fc577003f99606588bb3
```

<br>

### Aave Seatbelt reports

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/301.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/301.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/301_Polygon_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/301_Polygon_pending_0.md)

<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Polygon.

From a technical perspective, we have verified the [proposal payload](https://polygonscan.com/address/0xf8ad3689e88cfec0afa82b65681336140574dd69#code#F1#L14) correctly uses the BGD's Aave Config Engine of Aave v3 Polygon, in this case, to update the supply cap of MATICx the following way:
- Supply cap: 50'600'000 MATICx -> **62'000'000 MATICx**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
