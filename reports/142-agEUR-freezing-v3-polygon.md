# Proposal 142. Aave v3 Polygon - Freezing of agEUR

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=142](https://app.aave.com/governance/proposal/?proposalId=142)

<br>

### Governance forum discussion

[https://governance.aave.com/t/jeur-incident-plan-of-action/11379](https://governance.aave.com/t/jeur-incident-plan-of-action/11379)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

:ice_cube: freeze-asset

<br>

### Context

Following an exploit on the Midas protocol slightly affecting agEUR, this proposal freezes the agEUR asset on Aave v3 Polygon.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xd6b6fa147b33544ec0dca560d1cb05f9133aa0089b715bbe2398b7b75c7d1085](https://etherscan.io/tx/0xd6b6fa147b33544ec0dca560d1cb05f9133aa0089b715bbe2398b7b75c7d1085)

```
- id: 142
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x0000000000000000000000007b8fa4540246554e77fcff140f9114de00f8bb8d]
- withDelegatecalls: [true]
- startBlock: 16441993
- endBlock: 16461193
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xafa8d52094cc041ee20ca429e22b86ae20d6735b4067a617548ccc242bd5b264
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/142.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/142.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/142_fx_11_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/142_fx_11_0.md)


<br>

### Technical analysis

This is a cross-chain governance proposal, with [its payload](https://polygonscan.com/address/0x7b8fa4540246554e77fcff140f9114de00f8bb8d#contracts) interacting with the Aave v3 Polygon by calling `setReserveFreeze()` on the [Pool Configurator contract](https://polygonscan.com/address/0x8145eddDf43f50276641b55bd3AD95944510021E).

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD wrote the payload.

:x: With BGD writing the payload, at least another party reviewed it.
