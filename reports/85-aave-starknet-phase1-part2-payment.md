# Proposal 85. Aave <> StarkNet Phase 1 (Part 2). Second payment tranche

<br>

### Voting link
[https://app.aave.com/governance/proposal/?proposalId=85](https://app.aave.com/governance/proposal/?proposalId=85)

### Governance forum discussion
[https://governance.aave.com/t/request-for-approval-aave-starkware-phase-i/7145#payments-8](https://governance.aave.com/t/request-for-approval-aave-starkware-phase-i/7145#payments-8)

<br>

## BGD analysis

### Proposal types

:money_with_wings: funds-release

### Context

This proposal releases the second tranche of the previously approved Aave <> StarkNet Phase 1 project, accounting for 92'500 USDC.

### Proposal creation
Transaction: [https://etherscan.io/tx/0xff5db78bf3877d91eba493518255075baf91246a6a6c6b4caf98628a1c52b65d](https://etherscan.io/tx/0xff5db78bf3877d91eba493518255075baf91246a6a6c6b4caf98628a1c52b65d)
```
- id: 85
- creator: 0xb85fa70cf9ab580580d437bdea785b71631a8a7c
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x0e06e1618e11ae602539b8d70fb6b611272d8a71]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 15076044
- endBlock: 15095244
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x4866db95bac1722f825c8eaaebc47409068cc7075e6dda228effe10a71ac47b1
```

### Aave Seatbelt report
[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/085.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/085.md)

### Technical analysis
From a technical perspective, we have verified that the proposal payload does the following:

1. Transfers 92'500 aUSDC to the governance short executor from the [Aave V2 Ethereum Collector](https://etherscan.io/address/0x464C71f6c2F760DdA6093dCB91C24c39e5d6e18c#code), by calling `transfer()` on the [AaveEcosystemReserveController](https://etherscan.io/address/0x3d569673dAa0575c936c7c67c4E6AedA69CC630C#code).

2. Withdraws 92'500 USDC from the Aave V2 Ethereum [Pool](https://etherscan.io/address/0x7d2768dE32b0b80b7a3454c06BdAc94A69DDc7A9#code), to the funds recipient account defined on the payload.


### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

:white_check_mark: Only one payload used via delegatecall