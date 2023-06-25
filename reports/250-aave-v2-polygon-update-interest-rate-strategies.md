# Proposal 250. Aave v2 Polygon - update rate strategies and reserve factors

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=250](https://app.aave.com/governance/proposal/?proposalId=250)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-polygon-v2-parameter-update/12817](https://governance.aave.com/t/arfc-polygon-v2-parameter-update/12817)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the interest rate strategies of multiple assets on Aave v2 Polygon, together with several Reserve Factor configurations.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xe247bb653ecd593bed08400726fb9d53dfb8cb71bd04b94d9953de9b3e5b0666](https://etherscan.io/tx/0xe247bb653ecd593bed08400726fb9d53dfb8cb71bd04b94d9953de9b3e5b0666)

```
- id: 250
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000bbd2b7418395d1782f0016095c6a26487d184873]
- withDelegatecalls: [true]
- startBlock: 17532468
- endBlock: 17551668
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xc379a1c8444f75347501f2084ee21e0c47d376f14683119e7d238d37e72d93d5
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/250.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/250.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/250_Polygon_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/250_Polygon_pending_0.md)

<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Polygon.

The changes introduced by the payload on Aave v2 Polygon are the following (on rate strategy and reserve factors):

**[Aave v2 Polygon](https://polygonscan.com/address/0xbbd2b7418395d1782f0016095c6a26487d184873#code#F1#L31)**

DAI:

- Optimal usage ratio: 80% -> **71%**
- Variable slope 2: 75% -> **105%**
- RF: 10% -> **21%**

USDC:

- Optimal usage ratio: 90% -> **77%**
- Variable slope 2: 60% -> **134%**
- RF: 10% -> **23%**

USDC:

- Optimal usage ratio: 80% -> **52%**
- Variable slope 2: 100% -> **236%**
- RF: 10% -> **22%**

WBTC:

- Optimal usage ratio: 65% -> **37%**
- Variable slope 2: 300% -> **536%**
- RF: 20% -> **55%**

WETH:

- Optimal usage ratio: 65% -> **40%**
- Variable slope 2: 100% -> **167%**
- RF: 10% -> **45%**

WMATIC:

- Optimal usage ratio: 65% -> **48%**
- Variable slope 2: 300% -> **440%**
- RF: 20% -> **41%**

BAL:

- Optimal usage ratio: 80% -> **65%**
- Variable slope 2: 150% -> **236%**
- RF: 20% -> **32%**

CRV:

- Optimal usage ratio: 45% -> **25%**
- Variable slope 2: 300% -> **392%**
- RF: 20% -> **38%**

GHST:

- Optimal usage ratio: 45% -> **23%**
- Variable slope 2: 300% -> **413%**
- RF: 20% -> **60%**

LINK:

- Optimal usage ratio: 45% -> **25%**
- Variable slope 2: 300% -> **402%**
- RF: 10% -> **50%**

<br>

The updates are aligned with those defined in the Aave governance forum and Snapshot.

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Multiple payloads used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
