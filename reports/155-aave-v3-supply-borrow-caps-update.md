# Proposal 155. Aave v3 - Supply/borrow caps update on Polygon and Arbitrum

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=155](https://app.aave.com/governance/proposal/?proposalId=155)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-chaos-labs-supply-and-borrow-cap-updates-aave-v3-polygon-and-arbitrum-2023-02-07/11605](https://governance.aave.com/t/arc-chaos-labs-supply-and-borrow-cap-updates-aave-v3-polygon-and-arbitrum-2023-02-07/11605)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal is an update of supply and borrow caps affecting Aave v3 Polygon and Arbitrum, by Chaos Labs.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x0fe479989d4f2b6ddb0500087bc33eaffad83f30bcc0f0a337e77ead783724c8](https://etherscan.io/tx/0x0fe479989d4f2b6ddb0500087bc33eaffad83f30bcc0f0a337e77ead783724c8)

```
- id: 155
- creator: 0xbc540e0729b732fb14afa240aa5a047ae9ba7df0
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b,0x2e2b1f112c4d79a9d22464f0d345de9b792705f1]
- values: [0,0]
- signatures: [execute(address),execute(address)]
- calldatas: [0x000000000000000000000000060bea15af594fe9e0a243ca632f2c7d1935c70f,0x000000000000000000000000280e404338d9d8e50b11d6677b9c91ba86e0fd22]
- withDelegatecalls: [true,true]
- startBlock: 16643356
- endBlock: 16662556
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x6398bf1320d1347de159e8e387962ca4478d324c1b0664f7ea9afe2cbafa5e21
```

<br>

### Aave Seatbelt reports

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/155.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/155.md)


**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/155_fx_14_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/155_fx_14_0.md)

**Arbitrum**

Aave Seatbelt doesn't support Arbitrum yet.

<br>

### Technical analysis

From a technical perspective, we have verified that the proposal payload does the following changes on Polygon and Arbitrum:

1. Polygon:
  - BAL supply cap changed to **361'000 BAL**
  - EURS supply cap changed to **4'000'000 EURS**
  - EURS borrow cap changed to **947'000 EURS**
  - DAI supply cap changed to **45'000'000 DAI**
  - DAI borrow cap changed to **30'000'000 DAI**
  - USDC supply cap changed to **150'000'000 USDC**
  - USDC borrow cap changed to **100'000'000 USDC**
  - USDT supply cap changed to **45'000'000 USDT**
  - USDT borrow cap changed to **30'000'000 USDT**

2. Arbitrum
  - LINK supply cap changed to **677'000 LINK**
  - WETH supply cap changed to **35'280 WETH**



<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
