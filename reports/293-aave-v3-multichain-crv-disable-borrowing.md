# Proposal 293. Aave v3 Ethereum, Polygon - Disable CRV borrowing

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=293](https://app.aave.com/governance/proposal/?proposalId=293)

<br>

### Governance forum discussion

[https://governance.aave.com/t/post-vyper-exploit-crv-market-update-and-recommendations/14214/42](https://governance.aave.com/t/post-vyper-exploit-crv-market-update-and-recommendations/14214/42)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal disables borrowing of CRV on Aave v3 Ethereum and Polygon.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x378a16bb0e68c1f737ab9390866e6139cb59e87decd4c4aebf782409fdd607dd](https://etherscan.io/tx/0x378a16bb0e68c1f737ab9390866e6139cb59e87decd4c4aebf782409fdd607dd)

```
- id: 293
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x10bdbdeb8d3ff6273261dd7e9b90465000325dcb,0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0,0]
- signatures: [execute(),execute(address)]
- calldatas: [0x,0x000000000000000000000000fa6481b09c273d17701fb90427d6658a028edc18]
- withDelegatecalls: [true,true]
- startBlock: 17883678
- endBlock: 17902878
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xca79de3ab680e9cc6aa63f0b371364411c2a6083c8726d22466867bff1467ff3
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/293.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/293.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/293_Polygon_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/293_Polygon_pending_0.md)


<br>

### Technical analysis

We have verified both proposal payloads ([Ethereum](https://etherscan.io/address/0x10bdbdeb8d3ff6273261dd7e9b90465000325dcb#code#F1#L14) and [Polygon](https://polygonscan.com/address/0xfa6481b09c273d17701fb90427d6658a028edc18#code#F1#L14)) properly disable borrowing of CRV on Aave v3 Ethereum and Polygon, by using the BGD Config Engine.

The Polygon component uses correctly the Aave cross-chain governance system.

The proposal is consistent with the discussions on the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
