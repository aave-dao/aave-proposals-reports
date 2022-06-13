# Proposal 82. Renew AAVE allowance of the Aave Safety Module

<br>

### Voting link
[https://app.aave.com/governance/proposal/?proposalId=82](https://app.aave.com/governance/proposal/?proposalId=82)

### Governance forum discussion
[https://governance.aave.com/t/aip-renewal-of-safety-module-aave-allowance/8463](https://governance.aave.com/t/aip-renewal-of-safety-module-aave-allowance/8463)

<br>

## BGD analysis

### Proposal types

:shield: safety-module

:credit_card: funds-allowance

### Context
This proposal aims to extend the allowance of AAVE for safety incentives on the Aave Safety Module for two years at the current emission.

### Proposal creation
Transaction: [https://etherscan.io/tx/0xe213250115600557fcdd1a4a15f4d2e5692b20a9f82f46917617c1e643cfe63a](https://etherscan.io/tx/0xe213250115600557fcdd1a4a15f4d2e5692b20a9f82f46917617c1e643cfe63a)
```
- id: 82
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x83fba23163662149b33dbc05cf1312df6dcba72b]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 14955661
- endBlock: 14974861
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x495a8adb28587f0b208aaa0fcb19686c15cd344e5d360480220b0d2f1ff86694
```

### Aave Seatbelt report
[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/082.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/082.md)

### Technical analysis
**BGD has submitted this proposal**, and the proposal's payload [HERE](https://etherscan.io/address/0x83fba23163662149b33dbc05cf1312df6dcba72b#code) does the following:
- Through the controller smart contract of the AAVE ecosystem's reserve, resets the allowance of AAVE to 0 for both stkAAVE and stkABPT.
- Via the same controller, sets the allowance of AAVE to 401'500 (emission per second * 2 years) for both stkAAVE and stkABPT. 2 years was chosen for a good equilibrium of not-so-frequent update, and still keeping some funds' isolation.

The technical implementation of the proposal and tests can be found here [https://github.com/bgd-labs/renewal-aave-sm-allowance](https://github.com/bgd-labs/renewal-aave-sm-allowance).

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD wrote the payload.

:white_check_mark: With BGD writing the payload, at least another party reviewed it.
