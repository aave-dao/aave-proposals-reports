# Proposal 255. Aave v2 Ethereum - CRV risk parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=255](https://app.aave.com/governance/proposal/?proposalId=255)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-crv-aave-v2-ethereum-2023-06-15/13709](https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-crv-aave-v2-ethereum-2023-06-15/13709)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates multiple risk parameters of the CRV asset on Aave v2 Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xf254442d1450299fe7bd06717d9b76c4aedeb16c033f923ca88e49a9572d34be](https://etherscan.io/tx/0xf254442d1450299fe7bd06717d9b76c4aedeb16c033f923ca88e49a9572d34be)

```
- id: 255
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x317129b1bf6c65c2185fbbae0f452d8ecedb9ed9]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17585784
- endBlock: 17604984
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x8011346b7539d7041e50f33fa09632c0e977614d920b941de6d0b6f658d00116
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/255.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/255.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x317129b1bf6c65c2185fbbae0f452d8ecedb9ed9#code#F1#L12) properly changes the following risk parameters of CRV on Aave v2 Ethereum:

CRV
- LTV: 52% -> **49%**
- Liquidation Threshold: 58% -> **55%**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
