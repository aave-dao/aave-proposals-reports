# Proposal 367. Aave v2 Polygon - Reserve Factor updates

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=367](https://app.aave.com/governance/proposal/?proposalId=367)

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

Transaction: [https://etherscan.io/tx/0x2ec3826f8bc24c2aef69d89f8f55c167a1828813baed3db91d5d1edade3e7d96](https://etherscan.io/tx/0x2ec3826f8bc24c2aef69d89f8f55c167a1828813baed3db91d5d1edade3e7d96)

```
- id: 367
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000890000000000000000000000000000000000000000000000000000000000000001000000000000000000000000401b5d0294e23637c18fcc38b1bca814cda2637c0000000000000000000000000000000000000000000000000000000000000004]
- withDelegatecalls: [false]
- startBlock: 18549088
- endBlock: 18568288
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x998d4840e131431fe525407a13e5ca74f634066fd8ef0bee68629e83ac67b7bd
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/367.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/367.md)

**Payloads report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/4.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/4.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://polygonscan.com/address/0x3aE999AEf88072aC7fB702af1C362f47647962FC#code#F1#L13) properly changes the following Reserve Factors on Aave v2 Polygon:

WMATIC: 61% -> **66%**

WBTC: 75% -> **80%**

USDC: 43% -> **48%**

WETH: 65% -> **70%**

DAI: 41% -> **46%**

BAL: 52% -> **57%**

USDT: 42% -> **47%**


*There is no update on the Aave forum regarding this update, or the link attached on the AIP is wrong**. However, the update is consistent with the 5% period increase disclosed on the governance forum thread linked.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
