# Proposal 276. Aave v3 Polygon - MATICx supply cap update

<br>


### Voting link

[https://app.aave.com/governance/proposal/?proposalId=276](https://app.aave.com/governance/proposal/?proposalId=276)

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

Transaction: [https://etherscan.io/tx/0xe5d6b2a231de1090219046fb6b96ff131547ea3a88b53063f9a1ca0894a54655](https://etherscan.io/tx/0xe5d6b2a231de1090219046fb6b96ff131547ea3a88b53063f9a1ca0894a54655)

```
- id: 276
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000bacbe678e2c59343024fd5755262c7b0f77867d1]
- withDelegatecalls: [true]
- startBlock: 17693840
- endBlock: 17713040
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xdc2654339761e78195b693d8d90ee96531d71c9c1236612d94a22c62554e3a92
```

<br>

### Aave Seatbelt reports

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/276.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/276.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/276_Polygon_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/276_Polygon_pending_0.md)

<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Polygon.

From a technical perspective, we have verified the [proposal payload](https://polygonscan.com/address/0xbacbe678e2c59343024fd5755262c7b0f77867d1#code#F1#L13) correctly uses the BGD's Aave Config Engine of Aave v3 Polygon, in this case, to update the supply cap of MATICx the following way:
- Supply cap: 38'000'000 MATICx -> **50'600'000 MATICx**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
