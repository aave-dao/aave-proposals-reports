# Proposal 243. (Repetition of 240). Aave v3 Arbitrum - listing of LUSD

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=243](https://app.aave.com/governance/proposal/?proposalId=243)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-add-lusd-to-aave-v3-on-arbitrum/12858](https://governance.aave.com/t/arfc-add-lusd-to-aave-v3-on-arbitrum/12858)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists LUSD (LUSD Stablecoin, Liquity) on the Aave v3 Arbitrum pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x1d6a93244e7b888e4a4656388d87941e94d11c88ae24f7c4dcad3e0679d48f74](https://etherscan.io/tx/0x1d6a93244e7b888e4a4656388d87941e94d11c88ae24f7c4dcad3e0679d48f74)

```
- id: 243
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xd1b3e25fd7c8ae7caddc6f71b461b79cd4ddcfa3]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x00000000000000000000000098bc9dfa3cecb37f1bdeadc6e774d39082756b19]
- withDelegatecalls: [true]
- startBlock: 17479301
- endBlock: 17498501
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x5d3ef37d565163c470206fb12e7b47ccb2b12894938e6a6454863be49aad9cc6
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/243.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/243.md)

**Arbitrum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/243_Arbitrum_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/243_Arbitrum_pending_0.md)


<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Arbitrum.

The [proposal payload](https://arbiscan.io/address/0x98bc9dfa3cecb37f1bdeadc6e774d39082756b19#code#F1#L15) correctly uses the BGD's Aave Config Engine of Aave v3 Arbitrum, in this case, its listing features.

We have verified this payload respects the interface required by the v3 config engine and effectively configures the LUSD listing with the following initial parameters:

- The asset is enabled for borrowing and the interest rate strategy follows the parameters on the forum:
  - Base variable borrow: 0%
  - Variable borrow slope 1: 4%
  - Variable borrow slope 2: 87%
  - Optimal point: 80%

- The asset is not enabled as collateral
- Reserve Factor: 10%
- Supply cap: 900'000 LUSD
- Borrow cap: 900'000 LUSD
- No eMode category
- No isolation mode
- Flashlonable
- Not enabled for borrowing on isolation

The oracle used is the [Chainlink LUSD/USD feed](https://arbiscan.io/address/0x0411d28c94d85a36bc72cb0f875dfa8371d8ffff#readContract#F8).

The initial configuration is completely aligned with the description on the Aave governance forum.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
