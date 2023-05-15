# Proposal 224. Aave v2 Ethereum, Polygon - update multiple rate strategies

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=224](https://app.aave.com/governance/proposal/?proposalId=224)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-aave-v2-interest-rate-curve-recommendations-from-gauntlet-2023-04-21/12846](https://governance.aave.com/t/arfc-aave-v2-interest-rate-curve-recommendations-from-gauntlet-2023-04-21/12846)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the interest rate strategies of multiple assets on Aave v2 Ethereum and Polygon.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x05152e33582d861b7047254680588b249783be8d680936423f91bb90a74717cf](https://etherscan.io/tx/0x05152e33582d861b7047254680588b249783be8d680936423f91bb90a74717cf)

```
- id: 224
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x24bdacf6bbebaf567123da16cdb79a266597e92b,0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0,0]
- signatures: [execute(),execute(address)]
- calldatas: [0x,0x000000000000000000000000f22c8255ea615b3da6ca5cf5aecc8956bff07aa8]
- withDelegatecalls: [true,true]
- startBlock: 17247483
- endBlock: 17266683
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x6a96992b967855038741da685558e17d2f167dee2b41af0154d31499a574b940
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/224.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/224.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/224_fx_37_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/224_fx_37_0.md)

<br>

### Technical analysis

We have verified that on the non-Ethereum payloads, the proposal uses correctly the Aave cross-chain governance system to communicate with Polygon.

Regarding the changes on each we have verified they are the following.

**[Aave v2 Ethereum](https://etherscan.io/address/0x24bdacf6bbebaf567123da16cdb79a266597e92b#code#F1#L32)**

FRAX:

- Variable slope 2: 75% -> **100%**

GUSD:

- Optimal usage ratio: 80% -> **70%** (with `maxExcessUsageRatio` properly adjusted to 30%)
- Variable slope 2: 100% -> **150%**

USDP:

- Optimal usage ratio: 90% -> **80%** (with `maxExcessUsageRatio` properly adjusted to 20%)
- Variable slope 2: 60% -> **75%**

USDT:

- Variable slope 2: 75% -> **100%**
- Stable slope 2: 75% -> **100%**

WBTC:
- Variable slope 1: 8% -> **4%**

<br>

**[Aave v2 Polygon](https://polygonscan.com/address/0xf22c8255ea615b3da6ca5cf5aecc8956bff07aa8#code#F1#L90)**

USDT:

- Optimal usage ratio: 90% -> **80%** (with `maxExcessUsageRatio` properly adjusted to 20%)
- Variable slope 2: 60% -> **100%**
- Stable slope 2: 60% -> **100%**

WBTC:

- Variable slope 1: 8% -> **4%**


WETH:

- Variable slope 1: 8% -> **4%**

WMATIC:

- Optimal usage ratio: 45% -> **65%** (with `maxExcessUsageRatio` properly adjusted to 35%)
- Variable slope 1: 7% -> **6%**

<br>

The updates are aligned with those defined in the proposal's description, and the inconsistencies with the forum/Snapshot have been disclosed by the proposer [HERE](https://governance.aave.com/t/arfc-aave-v2-interest-rate-curve-recommendations-from-gauntlet-2023-04-21/12846/8), and are reasonable.

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Multiple payloads used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
