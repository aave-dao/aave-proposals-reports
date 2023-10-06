# Proposal 333. Treasury Management - Acquire GHO and replace AGD allowance

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=333](https://app.aave.com/governance/proposal/?proposalId=333)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-treasury-management-replace-agd-s-dai-allowance-with-gho-allowance/14631](https://governance.aave.com/t/arfc-treasury-management-replace-agd-s-dai-allowance-with-gho-allowance/14631)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposals swaps 228'000 aUSDC and 150'000 aUSDT to GHO via the AaveSwapper contract, in order to replace the current AGD (Aave Grants DAO) aDAI v2 allowance with GHO.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x73f3a66714a48ba13ea84e5a7180cee13c4323cc51e99f8d545bfd978fda6f31](https://etherscan.io/tx/0x73f3a66714a48ba13ea84e5a7180cee13c4323cc51e99f8d545bfd978fda6f31)

```
- id: 333
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x7fba17da9a96fb77a86229c975c91ded11dafa60]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 18269368
- endBlock: 18288568
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xe39c059166060f85b98f1c6ac25a0e954d21cae2f6420502859180e2d1f8fbe4
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/333.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/333.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x7fba17da9a96fb77a86229c975c91ded11dafa60#code#F1#L36) does the following:


1. The payload redeems 228'000 USDC and 150'000 from the Aave Ethereum Collector (held in aUSDC and aUSDT).
2. By interacting with the AaveSwapper smart contract, the payload creates 2 orders to swap both USDC and USDT previously withdrawn amounts to GHO.
3. Remove the existing allowance of aDAI (v2 Ethereum) from AGD (Aave Grants DAO).
4. Give 388'000 GHO allowance to AGD. It is important to highlight that it is possible that the amount of GHO will be slightly smaller due to slippage on the trade, but that should not create any problem.

After the payload is executed, off-chain the AaveSwapper will execute the swap to GHO via CowSwap/Milkman, and transfer the funds to the Aave Ethereum Collector. At that point, AGD will be able to claim funds.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
