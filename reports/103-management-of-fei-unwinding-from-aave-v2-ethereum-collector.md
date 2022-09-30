# Proposal 103. Management of FEI (aFEI) unwinding from Aave v2 Ethereum Collector

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=103](https://app.aave.com/governance/proposal/?proposalId=103)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-ethereum-v2-reserve-factor-afei-holding-update/9401](https://governance.aave.com/t/arc-ethereum-v2-reserve-factor-afei-holding-update/9401)

<br>

## BGD analysis

<br>

### Proposal types

:credit_card: funds-allowance

:moneybag: protocol-collector

<br>

### Context

Following the freezing process of FEI started on [proposal 96](https://app.aave.com/governance/proposal/96/), this next step redeems the FEI held by the Aave v2 Ethereum Collector, to exchange it for DAI on the Tribe DAO PSM, and re-supply this DAI on Aave v2 Ethereum on behalf of the Collector.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x92bc3fa981acbc8fbb2691f0af759109394c14f1c13abf5edd017e01edb19b8d](https://etherscan.io/tx/0x92bc3fa981acbc8fbb2691f0af759109394c14f1c13abf5edd017e01edb19b8d)

```
- id: 103
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x8dfd2255a9d38c182a14f49afcb8a4a4763c6098]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 15640489
- endBlock: 15659689
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x267dbabe4b9efc5aaa4b883462eb81b98ad717f7d3db4720420f2a58aa3b2cf9
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/103.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/103.md)

<br>

### Technical analysis

From a technical perspective, the proposal involves 2 smart contracts:

1. **The proposal payload ([RedeemFei](https://etherscan.io/address/0x8dfd2255a9d38c182a14f49afcb8a4a4763c6098#code))**. This smart contract gives allowance of aFEI to a Swapper one (more on 2)) and triggers its execution by calling `swapAllAvailable()`.
2. **The [aFEI->aDAI Swapper](https://etherscan.io/address/0x9A953AC1090C7014D00FD205D89c6BA1C219Af8b#code)**. This contract takes care of the of the technicalities of swapping the aFEI of the Aave Collector for DAI on the Tribe DAO PSM. Generally it does the following:
    - "Pulls" all the available aFEI from the Aave Collector, approved on 1).
    - Redeems aFEI to FEI.
    - Swaps the FEI to DAI on the Tribe DAO Fixed Price PSM.
    - Supplies back the DAI to Aave v2 Ethereum, on behalf of the Collector.


Given that the Swapper contract keeps allowance of aFEI after this operation, it is possible in the future to call `swapAllAvailable()` in a permissionless way, to repeat the process, whenever more aFEI is accrued on the Collector.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
