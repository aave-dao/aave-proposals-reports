# Proposal 271. Aave v3 Ethereum - activation of USDT as collateral

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=271](https://app.aave.com/governance/proposal/?proposalId=271)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-usdt-risk-parameters-update-aave-v3-eth-pool/13571](https://governance.aave.com/t/arfc-usdt-risk-parameters-update-aave-v3-eth-pool/13571)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal activates USDT as collateral asset on Aave v3 Ethereum.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x69d30f9e780ebbbbef907d5dfebc913f87e535543d18604cde32cd332db5531c](https://etherscan.io/tx/0x69d30f9e780ebbbbef907d5dfebc913f87e535543d18604cde32cd332db5531c)

```
- id: 271
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xeda5678486c73eac27e899a7037d2521bcff2e1c]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17678346
- endBlock: 17697546
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xc80e4c72db3a0b44eee77a5d938d28135d1f28e4ac7a7b001270d5c4c3bf45d4
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/271.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/271.md)


<br>

### Technical analysis

The [proposal payload](https://etherscan.io/address/0xeda5678486c73eac27e899a7037d2521bcff2e1c#code#F1#L13) correctly uses the BGD's Aave Config Engine of Aave v3 Ethereum, in this case, to configure USDT as collateral with the following parameters:
- LTV: 74%
- Liquidation Threshold: 76%
- Liquidation Bonus: 4.5%
- Liquidation Protocol fee: 10%

The initial configuration is completely aligned with the [pre-approved by the community on Snapshot](https://snapshot.org/#/aave.eth/proposal/0x3690a2555731c402ac5dbcd225bdbc64f0bd11991d4d391d2682eb77b5dfa2a6)


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
