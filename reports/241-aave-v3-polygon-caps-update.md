# Proposal 241. Aave v3 Polygon - stMATIC, MATICX supply caps update

<br>


### Voting link

[https://app.aave.com/governance/proposal/?proposalId=241](https://app.aave.com/governance/proposal/?proposalId=241)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-polygon-v3-supply-cap-update-2023-05-21/13161](https://governance.aave.com/t/arfc-polygon-v3-supply-cap-update-2023-05-21/13161)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the supply caps of stMATIC and MATICX on Aave v3 Polygon.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xda762a8b7425ecb10ae14fc1f22faedccfee7c4f68d7342ad2352c9fca272883](https://etherscan.io/tx/0xda762a8b7425ecb10ae14fc1f22faedccfee7c4f68d7342ad2352c9fca272883)

```
- id: 241
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x00000000000000000000000076884cafecf1f7d4146da6c4053b18b76bf6ed14]
- withDelegatecalls: [true]
- startBlock: 17458431
- endBlock: 17477631
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xf76d79693a81a1c0acd23c6ee151369752142b0d832daeaef9a4dd9f8c4bc7ce
```

<br>

### Aave Seatbelt reports

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/241.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/241.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/241_Polygon_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/241_Polygon_pending_0.md)

<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Polygon.

From a technical perspective, we have verified the [proposal payload](https://polygonscan.com/address/0x76884cafecf1f7d4146da6c4053b18b76bf6ed14#code#F1#L14) correctly uses the BGD's Aave Config Engine of Aave v3 Polygon, in this case, to update supply caps the following way:

- stMATIC supply cap: 32'000'000 stMATIC -> **40'000'000 stMATIC**
- MATICX supply cap: 32'000'000 MATICX -> **40'000'000 MATICX**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
