# Proposal 196. Aave v3 Ethereum, Arbitrum, Optimism - add FLASH_BORROWER_ROLE to DefiSaver smart contracts

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=196](https://app.aave.com/governance/proposal/?proposalId=196)

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

This proposal sets FLASH_BORROWER_ROLE to different DefiSaver smart contracts on Aave v3 Ethereum, Arbitrum and Optimism. This will allow those contract to not be submitted to the payment of any fee to Aave when executing flash loans.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xe932beaa44281bd513e27f10f637f79b2dd1dd07670dc066d0bd94714dc1251a](https://etherscan.io/tx/0xe932beaa44281bd513e27f10f637f79b2dd1dd07670dc066d0bd94714dc1251a)

```
- id: 196
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x70e933079a87aebfed930eb0516efec041421153,0xd1b3e25fd7c8ae7caddc6f71b461b79cd4ddcfa3,0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711]
- values: [0,0,0]
- signatures: [execute(),execute(address),execute(address)]
- calldatas: [0x,0x00000000000000000000000076b19d3c129bfddb16e1ddb9eeef1db378bfb379,0x000000000000000000000000510b59f8258cf0bbeca9477fc774001b58df9a09]
- withDelegatecalls: [true,true,true]
- startBlock: 16981726
- endBlock: 17000926
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x20e3d493585740b9e4e2c3a4238b979907f2a7de7fc200f7ac109c73a493a57f
```

<br>

### Aave Seatbelt report

**Ethereum report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/196.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/196.md)

**Optimism report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/196_optimism_11_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/196_optimism_11_0.md)

**Arbitrum report**

Aave Seatbelt doesn't support Arbitrum yet.


<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system for the non-Ethereum payloads, which together with Ethereum's do the following:

**[Ethereum payload](https://etherscan.io/address/0x70e933079a87aebfed930eb0516efec041421153#code#F15#L1)**

The proposal payload properly gives `FLASH_BORROWER_ROLE` role to the contracts from Defisaver (FLAave, FLAction) interacting with Aave v3 Ethereum, by calling the `addFlashBorrower()` function on the Aave v3 Ethereum ACL Manager contract.

**[Arbitrum payload](https://arbiscan.io/address/0x76b19d3c129bfddb16e1ddb9eeef1db378bfb379#code#F15#L1)**

The proposal payload properly gives `FLASH_BORROWER_ROLE` role to the contracts from Defisaver (FLAave, FLAction) interacting with Aave v3 Arbitrum, by calling the `addFlashBorrower()` function on the Aave v3 Arbitrum ACL Manager contract.

**[Optimism payload](https://optimistic.etherscan.io/address/0x510b59f8258cf0bbeca9477fc774001b58df9a09#code#F15#L1)**

The proposal payload properly gives `FLASH_BORROWER_ROLE` role to the contracts from Defisaver (FLAave, FLAction) interacting with Aave v3 Optimism, by calling the `addFlashBorrower()` function on the Aave v3 Optimism ACL Manager contract.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
