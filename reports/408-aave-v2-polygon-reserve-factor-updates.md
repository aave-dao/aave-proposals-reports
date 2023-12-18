# Proposal 408. Aave v2 Polygon - Reserve Factor updates

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=408](https://app.aave.com/governance/proposal/?proposalId=408)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937](https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937)

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

Transaction: [https://etherscan.io/tx/0x166fff33348da46275d7a5771fa3fa6396faa72369c5d40bafc3c5e0e70e49e6](https://etherscan.io/tx/0x166fff33348da46275d7a5771fa3fa6396faa72369c5d40bafc3c5e0e70e49e6)

```
- id: 408
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000890000000000000000000000000000000000000000000000000000000000000001000000000000000000000000401b5d0294e23637c18fcc38b1bca814cda2637c0000000000000000000000000000000000000000000000000000000000000013]
- withDelegatecalls: [false]
- startBlock: 18797411
- endBlock: 18816611
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x4aa84545f2e5cbe002fb73fa28aeb809e2b48f5f2d179b14595731cb65c82ef2
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/408.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/408.md)

**Payloads report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/19.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/19.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://polygonscan.com/address/0x15135198E254259899e472C4D2Aa566fEC59077D#code#F1#L14) properly changes the following Reserve Factors on Aave v2 Polygon:

WMATIC: 71% -> **76%**

WBTC: 85% -> **90%**

USDC: 53% -> **58%**

WETH: 75% -> **80%**

DAI: 51% -> **56%**

USDT: 52% -> **57%**


*There is no update on the Aave forum regarding this update, or the link attached on the AIP is wrong**. However, the update is consistent with the 5% period increase disclosed on the governance forum thread linked.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
