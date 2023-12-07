# Proposal 393. Aave v2 Polygon - Reserve Factor updates

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=393](https://app.aave.com/governance/proposal/?proposalId=393)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937/5](https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937/5)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal increases the Reserve Factor parameter on multiple Aave v2 Polygon assets, with the objective of incentivising migrations to Aave v3 Polygon.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x939d79212d7a0535232f45d624249aef05257167645aa14b4ec84b30d6177942](https://etherscan.io/tx/0x939d79212d7a0535232f45d624249aef05257167645aa14b4ec84b30d6177942)

```
- id: 393
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000890000000000000000000000000000000000000000000000000000000000000001000000000000000000000000401b5d0294e23637c18fcc38b1bca814cda2637c000000000000000000000000000000000000000000000000000000000000000f]
- withDelegatecalls: [false]
- startBlock: 18718843
- endBlock: 18738043
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x3ecc07c9638cfe8fd8bb1a3cf8df0e82ed2d10e2c67381f533bbfb3b34bd5711
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/393.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/393.md)

**Payloads report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/15.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/15.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://polygonscan.com/address/0x7f88576D829C82E7f3BDDEFc67A143E83AC1d615#code#F1#L13) properly changes the following Reserve Factors on Aave v2 Polygon:

WMATIC: 66% -> **71%**

WBTC: 80% -> **85%**

USDC: 48% -> **53%**

WETH: 70% -> **75%**

DAI: 46% -> **51%**

BAL: 57% -> **99%**

USDT: 47% -> **52%**


*There is no update on the Aave forum regarding this update, or the link attached on the AIP is wrong**. However, the update is consistent with the 5% period increase disclosed on the governance forum thread linked.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
