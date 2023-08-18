# Proposal 296. Aave v3 Ethereum - LUSD risk parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=296](https://app.aave.com/governance/proposal/?proposalId=296)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-activate-lusd-as-collateral-on-aave-v3-eth-pool/14199](https://governance.aave.com/t/arfc-activate-lusd-as-collateral-on-aave-v3-eth-pool/14199)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal enables LUSD as collateral on Aave v3 Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x204ec620c3c014ee22dd8883773079054f89e1f78bb2823fcf23440f8297caa3](https://etherscan.io/tx/0x204ec620c3c014ee22dd8883773079054f89e1f78bb2823fcf23440f8297caa3)

```
- id: 296
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x96b3fe1bcc88903bcdb032b09fbb16ee0f908b43]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17899467
- endBlock: 17918667
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x0d2cc4c8c0d7a78fb60b11348eaec91b7b005df1ee36f1fa45b8ace6208f8a41
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/296.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/296.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x96b3fe1bcc88903bcdb032b09fbb16ee0f908b43#code#F1#L13) properly activates LUSD as collateral (non-isolated) with the following parameters:

- LTV: 77%
- Liquidation Threshold: 80%
- Liquidation Bonus: 4.5%
- Liquidation Protocol fee: 10%

The proposal is consistent with the discussions on the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
