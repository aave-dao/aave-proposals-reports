# Proposal 318. Aave v3 Arbitrum, Polygon, Optimism - Freezing of MAI

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=318](https://app.aave.com/governance/proposal/?proposalId=318)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-recommendations-for-mai-mimatic-2023-09-08/14799](https://governance.aave.com/t/arfc-recommendations-for-mai-mimatic-2023-09-08/14799)

<br>

## BGD analysis

<br>

### Proposal types

:ice_cube: freeze-asset

<br>

### Context

Following a important de-peg of MAI, this proposal freezes and sets its LTV to 0 on Aave v3 Arbitrum, Optimism and Polygon.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x83ae1e3025b581271f7c4ca6ba2a3e0b6986dcc90a0ff2a06fedfdfd64a11aec](https://etherscan.io/tx/0x83ae1e3025b581271f7c4ca6ba2a3e0b6986dcc90a0ff2a06fedfdfd64a11aec)

```
- id: 318
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xd1b3e25fd7c8ae7caddc6f71b461b79cd4ddcfa3,0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711,0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0,0,0]
- signatures: [execute(address),execute(address),execute(address)]
- calldatas: [0x000000000000000000000000f22c8255ea615b3da6ca5cf5aecc8956bff07aa8,0x00000000000000000000000024bdacf6bbebaf567123da16cdb79a266597e92b,0x0000000000000000000000002ee993533a482fe0f22d0fdf1b84ae1a0537e5ed]
- withDelegatecalls: [true,true,true]
- startBlock: 18101900
- endBlock: 18121100
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xc74f19fc8bb41498edc38f2da7cbc45e2e6d8adb1d28e50793df07328fb56377
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/318.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/318.md)

**Arbitrum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/318_Arbitrum_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/318_Arbitrum_pending_0.md)

**Optimism**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/318_Optimism_pending_2.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/318_Optimism_pending_2.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/318_Polygon_pending_1.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/318_Polygon_pending_1.md)

<br>

### Technical analysis

We have verified the following proposal payloads properly use Aave cross-chain governance to freeze the MAI asset on the different Aave v3 instances, and set its LTV to 0.

[Arbitrum payload](https://arbiscan.io/address/0xf22c8255ea615b3da6ca5cf5aecc8956bff07aa8#code#F1#L22)

[Optimism payload](https://optimistic.etherscan.io/address/0x24bdacf6bbebaf567123da16cdb79a266597e92b#code#F1#L47)

[Polygon payload](https://polygonscan.com/address/0x2ee993533a482fe0f22d0fdf1b84ae1a0537e5ed#code#F1#L72)

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the payload before the proposal was submitted.

:x: Only one payload used via delegatecall

:question: BGD reviewed the procedure followed to submit the proposal.