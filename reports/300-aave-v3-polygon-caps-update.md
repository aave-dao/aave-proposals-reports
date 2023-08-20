# Proposal 300. Aave v3 Polygon - stMATIC supply cap update

<br>


### Voting link

[https://app.aave.com/governance/proposal/?proposalId=300](https://app.aave.com/governance/proposal/?proposalId=300)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-supply-cap-stmatic-polygon/14355](https://governance.aave.com/t/arfc-supply-cap-stmatic-polygon/14355)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the supply cap of stMATIC on Aave v3 Polygon.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x0299f566658d20b892367e08152e4856a235a3a96c5efe0ca5663de76ebe1df2](https://etherscan.io/tx/0x0299f566658d20b892367e08152e4856a235a3a96c5efe0ca5663de76ebe1df2)

```
- id: 300
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000f28e5a2f04b6b74741579daee1fc164978d2d646]
- withDelegatecalls: [true]
- startBlock: 17930100
- endBlock: 17949300
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xe489f78a8a937c83a32ae6a7c7cdd8119c3e8d0b2f59d7f8336152b32361127a
```

<br>

### Aave Seatbelt reports

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/300.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/300.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/300_Polygon_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/300_Polygon_pending_0.md)

<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Polygon.

From a technical perspective, we have verified the [proposal payload](https://polygonscan.com/address/0xf28e5a2f04b6b74741579daee1fc164978d2d646#code#F1#L31) correctly uses the BGD's Aave Config Engine of Aave v3 Polygon, in this case, to update the supply cap of stMATIC the following way:
- Supply cap: 40'000'000 stMATIC -> **57'000'000 stMATIC**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
