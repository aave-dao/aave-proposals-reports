# Proposal 235 (Repetition of 196). Aave v3 Optimism - add FLASH_BORROWER_ROLE to DefiSaver smart contracts

<br>

### Voting link

[https://app.aave.com/governance/proposal/235](https://app.aave.com/governance/proposal/235)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-add-defi-saver-to-flashborrowers-on-aave-v3/12410](https://governance.aave.com/t/arfc-add-defi-saver-to-flashborrowers-on-aave-v3/12410)

<br>

## BGD analysis

<br>

### Proposal types

:passport_control: roles

<br>

### Context

This proposal sets FLASH_BORROWER_ROLE to different DefiSaver smart contracts on Aave v3 Optimism. This will allow those contract to not be submitted to the payment of any fee to Aave when executing flash loans.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xd3e4c1c582894091b0f2861c6225bb3e4274a096e599858f2a81333fc0dd9223](https://etherscan.io/tx/0xd3e4c1c582894091b0f2861c6225bb3e4274a096e599858f2a81333fc0dd9223)

```
- id: 235
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000510b59f8258cf0bbeca9477fc774001b58df9a09]
- withDelegatecalls: [true]
- startBlock: 17342197
- endBlock: 17361397
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x52affc618852d41e36f23c5c5c9e0d888e584fe4afeb52923c28bffb5986982d
```

<br>

### Aave Seatbelt report

**Ethereum report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/235.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/235.md)

**Optimism report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/235_Optimism_11.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/235_Optimism_11.md)


<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system with the payload doing the following:

**[Optimism payload](https://optimistic.etherscan.io/address/0x510b59f8258cf0bbeca9477fc774001b58df9a09#code#F15#L14)**

The proposal payload properly gives `FLASH_BORROWER_ROLE` role to the contracts from Defisaver (FLAave, FLAction) interacting with Aave v3 Optimism, by calling the `addFlashBorrower()` function on the Aave v3 Optimism ACL Manager contract.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
