# Proposal 124. Aave v2 Polygon - Risk Parameter Updates

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=124](https://app.aave.com/governance/proposal/?proposalId=124)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-risk-parameter-updates-for-aave-v2-polygon-and-aave-v3-avax-2022-11-23/10793](https://governance.aave.com/t/arc-risk-parameter-updates-for-aave-v2-polygon-and-aave-v3-avax-2022-11-23/10793)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

:link: :bridge_at_night: cross-chain execution

:ice_cube: freeze-asset

<br>

### Context

This proposal is an update of risk parameters on Aave v2 Polygon by Gauntlet, to freeze multiple assets, given the current situation of volatility in the market.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x4ffed87f5d3f3b5700eb1e65c3a4981d06e3b93d20da6dd741b42d4b69e10172](https://etherscan.io/tx/0x4ffed87f5d3f3b5700eb1e65c3a4981d06e3b93d20da6dd741b42d4b69e10172)

```
- id: 124
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x00000000000000000000000031976dc2ea27e75cc5a3687ed594d17127f9b72e]
- withDelegatecalls: [true]
- startBlock: 16044555
- endBlock: 16063755
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xdef650b98b37aece779f9776f867858c1535cbd4d943f40f314d3e9047d040c7
```

<br>

### Aave Seatbelt report

**Ethereum report:**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/124.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/124.md)

**Polygon report:**
[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/124_fx_7_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/124_fx_7_0.md)

<br>

### Technical analysis

Like on every Aave cross-chain proposal, this one follows the procedure defined on [https://github.com/bgd-labs/aave-v3-crosschain-listing-template](https://github.com/bgd-labs/aave-v3-crosschain-listing-template). This means that after execution on Ethereum, the proposal payload will be queued on the Polygon side of the cross-chain infrastructure and, after the timelock there, will be open for execution.

Assuming that the cross-chain flow works properly, we have verified from a technical perspective that the payload will effectively freeze the following assets, by calling `freezeReserve()` on the [Aave v2 Polygon Configurator](https://polygonscan.com/address/0x26db2B833021583566323E3b8985999981b9F1F3):

- BAL
- CRV
- DPI
- GHST
- LINK
- SUSHI

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
