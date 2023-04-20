# Proposal 205. Aave v3 Optimism - Risk params update

<br>

**!!! The title and description of the submitted proposal is incorrect due to an error on the IPFS reference used. This proposal updates risk parameters on Optimism, not supply/borrow caps on Arbitrum !!!**


### Voting link

[https://app.aave.com/governance/proposal/?proposalId=205](https://app.aave.com/governance/proposal/?proposalId=205)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-aave-v3-optimism-2023-03-22/12421](https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-aave-v3-optimism-2023-03-22/12421)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the risk parameters of WBTC and DAI on Aave v3 Optimism.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x1bd2e5e01c505ab8f412391ed764b2d0313b974d8e73e02fcab3f01132e46da0](https://etherscan.io/tx/0x1bd2e5e01c505ab8f412391ed764b2d0313b974d8e73e02fcab3f01132e46da0)

```
- id: 205
- creator: 0xbc540e0729b732fb14afa240aa5a047ae9ba7df0
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000c4421eaf9087aa0b8f453c130dc024c3eb3a34d7]
- withDelegatecalls: [true]
- startBlock: 17075554
- endBlock: 17094754
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x3153da673854d10ae6350b2508577a1d09d5486269b6501e15a557ec7fd73cb5
```

<br>

### Aave Seatbelt reports

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/205.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/205.md)


**Optimism**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/205_optimism_12_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/205_optimism_12_0.md)


<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Optimism.

From a technical perspective, we have verified the [proposal payload](https://optimistic.etherscan.io/address/0xc4421eaf9087aa0b8f453c130dc024c3eb3a34d7#code#F22#L1) correctly uses the new [BGD's Aave Config Engine of Aave v3 Optimism](https://optimistic.etherscan.io/address/0x7a9a9c14b35e58ffa1cc84ab421ace0fdcd289e3#code#F18#L1), in this case, to update the following risk parameters:

- WBTC:
  - LTV: 70% -> **73%**
  - Liquidation Threshold: 75% -> **78%**
  - Liquidation Bonus: 9.4% -> **8.5%**
- DAI:
  - LTV: 75% -> **78%**
  - Liquidation Threshold: 80% -> **83**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
