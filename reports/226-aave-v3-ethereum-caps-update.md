# Proposal 226. Aave v3 Ethereum - Caps update

<br>


### Voting link

[https://app.aave.com/governance/proposal/?proposalId=226](https://app.aave.com/governance/proposal/?proposalId=226)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-gauntlet-recommendations-for-lusd-eth-v3/13039](https://governance.aave.com/t/arc-gauntlet-recommendations-for-lusd-eth-v3/13039)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the borrow cap of LUSD on Aave v3 Ethereum.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xeda0b55f96a728d23dca9944a1a24a8ed258789d4fe490c008bc219dbf3e2ceb](https://etherscan.io/tx/0xeda0b55f96a728d23dca9944a1a24a8ed258789d4fe490c008bc219dbf3e2ceb)

```
- id: 226
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x0568a3aeb8e78262deff75ee68fac20ae35ffa91]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17276665
- endBlock: 17295865
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x37e7b80ec62a713b147db9c55d9cbd6b781ec16f38c7b4a4eaeaece7dc0fffae
```

<br>

### Aave Seatbelt reports

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/226.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/226.md)

<br>

### Technical analysis

From a technical perspective, we have verified the [proposal payload](https://etherscan.io/address/0x0568a3aeb8e78262deff75ee68fac20ae35ffa91#code#F1#L1) correctly uses the new [BGD's Aave Config Engine of Aave v3 Ethereum](https://etherscan.io/address/0xE202F2fc4b6A37Ba53cfD15bE42a762A645FCA07#code#F18#L1), to update the LUSD borrow cap from 2'400'000 LUSD to **4'000'000 LUSD**.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
