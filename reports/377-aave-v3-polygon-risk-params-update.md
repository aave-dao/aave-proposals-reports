# Proposal 377. Aave v3 Polygon - stMATIC/MATICx risk parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=377](https://app.aave.com/governance/proposal/?proposalId=377)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-gauntlet-recommendation-to-lower-stmatic-maticx-non-emode-lt-pt-2/15314](https://governance.aave.com/t/arfc-gauntlet-recommendation-to-lower-stmatic-maticx-non-emode-lt-pt-2/15314)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal reduces the Liquidation Threshold (LT) and LTV of stMATIC and MATICx on Aave v3 Polygon, on non-eMode.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xfe06fc36e62323ce8d4d635391f218b4602de59c70307cc9da263b0b749bdf00](https://etherscan.io/tx/0xfe06fc36e62323ce8d4d635391f218b4602de59c70307cc9da263b0b749bdf00)

```
- id: 377
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000890000000000000000000000000000000000000000000000000000000000000001000000000000000000000000401b5d0294e23637c18fcc38b1bca814cda2637c000000000000000000000000000000000000000000000000000000000000000b]
- withDelegatecalls: [false]
- startBlock: 18623092
- endBlock: 18642292
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x4989045af890034b671390e0bd573cf61bba6d3f20bfbb784abe1c420f7ec95d
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://raw.githubusercontent.com/bgd-labs/seatbelt-for-ghosts/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/377.md](https://raw.githubusercontent.com/bgd-labs/seatbelt-for-ghosts/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/377.md)

**Payload report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/11.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/11.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://polygonscan.com/address/0x54dC357F7461BcEEE5BdbA80996f5CB7d7512445#code#F1#L16) properly doing the following updates on Aave v3 Polygon, via the Config Engine:

*stMATIC*
- LT: 60% -> **56%**

*MATICx*
- LT: 62% -> **58%**

The proposal is consistent with the discussions on the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
