# Proposal 199. Aave v3 Polygon - WMATIC, BAL caps updates

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=199](https://app.aave.com/governance/proposal/?proposalId=199)

<br>

### Governance forum discussions

[https://governance.aave.com/t/arfc-wmatic-supply-cap-increase/12046](https://governance.aave.com/t/arfc-wmatic-supply-cap-increase/12046)

[https://governance.aave.com/t/arfc-polygon-v3-bal-supply-borrow-cap-increase/12505/3](https://governance.aave.com/t/arfc-polygon-v3-bal-supply-borrow-cap-increase/12505/3)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the borrow caps of WMATIC and BAL on Aave v3 Polygon.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xe7ae58329077e4c60bdab2a932fbd7d6255892d7cd6dd597c1e8b5b13b56b293](https://etherscan.io/tx/0xe7ae58329077e4c60bdab2a932fbd7d6255892d7cd6dd597c1e8b5b13b56b293)

```
- id: 199
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x00000000000000000000000047938b58f104b4e06a5572faa9cb3c3cd53f15a4]
- withDelegatecalls: [true]
- startBlock: 16996904
- endBlock: 17016104
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x61c411588a88828064b4227c619e88e3e11fed626719cac28b808faeaeacabc1
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/199.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/199.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/199_fx_27_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/199_fx_27_0.md)

<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Polygon.

Regarding the Polygon side, we have verified the [proposal payload](https://polygonscan.com/address/0x47938b58f104b4e06a5572faa9cb3c3cd53f15a4#code#F21#L13) correctly updates the supply cap of WMATIC from 47'000'000 to **66'000'000 WMATIC**, together with the borrow cap of BAL from 256'140 to **290'000 BAL**.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
