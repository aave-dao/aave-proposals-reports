# Proposal 233. Aave v3 Polygon, Arbitrum, Optimism - e-mode risk params updates

<br>


### Voting link

[https://app.aave.com/governance/proposal/?proposalId=233](https://app.aave.com/governance/proposal/?proposalId=233)

<br>

### Governance forum discussions

[https://governance.aave.com/t/gauntlet-aave-v3-e-mode-methodology/12278](https://governance.aave.com/t/gauntlet-aave-v3-e-mode-methodology/12278)


<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates risk parameters of the USD-correlated e-mode category on Aave v3 Polygon, Arbitrum and Optimism.

**IMPORTANT. This proposal causes user liquidations, but this has been extensively disclosed and acknowledged by the proposer (Gauntlet) for the community**

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xf94ee0fdde6965c42dcb3e07e66db8b11deffecbf1cc93310b6ffb970f17fb28](https://etherscan.io/tx/0xf94ee0fdde6965c42dcb3e07e66db8b11deffecbf1cc93310b6ffb970f17fb28)

```
- id: 233
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xd1b3e25fd7c8ae7caddc6f71b461b79cd4ddcfa3,0x158a6bc04f0828318821bae797f50b0a1299d45b,0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711]
- values: [0,0,0]
- signatures: [execute(address),execute(address),execute(address)]
- calldatas: [0x000000000000000000000000142dcaec322aaa25141b2597bf348487adbd596d,0x00000000000000000000000024bdacf6bbebaf567123da16cdb79a266597e92b,0x000000000000000000000000f22c8255ea615b3da6ca5cf5aecc8956bff07aa8]
- withDelegatecalls: [true,true,true]
- startBlock: 17325938
- endBlock: 17345138
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x597779e8a7564df81730fbb0522ee52147427851c335df92bc297d332de34dc2
```

<br>

### Aave Seatbelt reports

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/233.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/233.md)


**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/233_fx_43_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/233_fx_43_0.md)

**Optimisim**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/233_optimism_18_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/233_optimism_18_0.md)

**Arbitrum**

Aave Seatbelt doesn't support Arbitrum yet.


<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system in the parts communicating with Polygon, Arbitrum and Optimism.

Regarding each payload, the changes applied are the following:

**[Polygon](https://polygonscan.com/address/0x24bdacf6bbebaf567123da16cdb79a266597e92b#code#F1#L90)**

- USD-correlated e-mode (`eModeCategory` 1):
  - LTV: 97% -> **93%**
  - Liquidation Threshold: 97.5% -> **95%**

**[Arbitrum](https://arbiscan.io/address/0x142dcaec322aaa25141b2597bf348487adbd596d#code#F1#L42)**

- USD-correlated e-mode (`eModeCategory` 1):
  - LTV: 97% -> **93%**
  - Liquidation Threshold: 97.5% -> **95%**

**[Optimism](https://optimistic.etherscan.io/address/0xf22c8255ea615b3da6ca5cf5aecc8956bff07aa8#code#F1#L187)**

- USD-correlated e-mode (`eModeCategory` 1):
  - LTV: 97% -> **93%**
  - Liquidation Threshold: 97.5% -> **95%**

<br>

The caps updates are aligned with those defined in the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
