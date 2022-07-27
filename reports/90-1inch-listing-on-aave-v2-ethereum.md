# Proposal 90. (Repetition of Proposal 89). Add 1INCH to Aave V2 Ethereum

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=90](https://app.aave.com/governance/proposal/?proposalId=90)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-add-1inch-as-collateral/8056](https://governance.aave.com/t/arc-add-1inch-as-collateral/8056)

<br>

## BGD analysis

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists the [1INCH](https://etherscan.io/address/0x111111111117dc0aa78b770fa6a738034120c302) asset on Aave V2 Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xbd74507b8cad721a8dc78e2d4998a635e1b8bae469552e7552ad48efc5b1fcef](https://etherscan.io/tx/0xbd74507b8cad721a8dc78e2d4998a635e1b8bae469552e7552ad48efc5b1fcef)

```
- id: 90
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xd417d07c20e31f6e129fa68182054b641fbec8bd]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 15218841
- endBlock: 15238041
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x0807c1081243b87ff499e9af640afab121f24a693b289c11ea301cad1fd51ccf
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/090.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/090.md)

<br>

### Technical analysis

This proposal lists the 1INCH token on Aave V2 Ethereum as borrowing asset and collateral, via the proposal payload [OneInchListingPayload](https://etherscan.io/address/0xd417d07c20e31f6e129fa68182054b641fbec8bd#code).

We have verified that the listing parameters are consistent with the ones pre-approved on [Snapshot](https://snapshot.org/#/aave.eth/proposal/0x2ea76814a0dfcad7ea1a7b3c597f059a8d574f8143886b23043918998505f5a7), being:

- **LTV**: 40%
- **Liquidation Threshold**: 50%
- **Liquidation Bonus**: 8.5%
- **Reserve Factor**: 20%
- **Enabled to borrow**.
- **Not enabled to borrow at stable mode**.

Some remarks from BGD:

- 1INCH properly reuses an interest rate strategy defining the exact same parameters.
- We have verified that the implementations used for aToken, variableDebtToken and stableDebtToken are the same as existing ones for other assets listed.
- We have verified that, before the listing itself, the 1INCH/ETH feed is correctly configured on the Aave oracle.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
