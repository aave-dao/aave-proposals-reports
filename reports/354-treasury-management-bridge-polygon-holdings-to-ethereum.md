# Proposal 354. Treasury Management - Bring Polygon Collector's holdings to Ethereum
<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=354](https://app.aave.com/governance/proposal/?proposalId=354)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-transfer-assets-from-polygon-to-ethereum-treasury/15044](https://governance.aave.com/t/arfc-transfer-assets-from-polygon-to-ethereum-treasury/15044)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposals bridges DAI, CRV and BAL from the Aave Polygon Collector to the Aave Ethereum Collector, by using the `AavePolEthERC20Bridge` created by Llama on their previous engagement.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xb4c83d70671ad5b03f2dcaa749b7f3be8a8c22e19396bfca1fbfcca321e3bbf6](https://etherscan.io/tx/0xb4c83d70671ad5b03f2dcaa749b7f3be8a8c22e19396bfca1fbfcca321e3bbf6)

```
- id: 354
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000ccafbbbd68bb9b1a5f1c6ac948ed1944429f360a]
- withDelegatecalls: [true]
- startBlock: 18421499
- endBlock: 18440699
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xf763d59548ffa89cfbf72d7bada1991158abe4bd30e31bce58dbdd377151031f
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/354.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/354.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/354_Polygon_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/354_Polygon_pending_0.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://polygonscan.com/address/0xccafbbbd68bb9b1a5f1c6ac948ed1944429f360a#code#F1#L20) does the following:
1. Redeems 1'500'000 aDAI, ~9'523 aCRV and ~1'827 aBAL (all v2 Polygon) to DAI, CRV and BAL.
2. Transfer the DAI, CRV and BAL to the Aave Polygon <> Ethereum Collector bridge.
3. Call `bridge()` on the Aave Polygon <> Ethereum Collector bridge for each asset, to trigger the bridging to Ethereum.

It is important to highlight that, once this is executed on the Polygon side, and after waiting the message bridging delay from Polygon to Ethereum, the proposer (or any address, being permissionless) will need to trigger the claim of DAI, CRV and BAL on Ethereum, directed to the Ethereum Collector.

The payload is consistent with the description in the governance forum and Snapshot.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
