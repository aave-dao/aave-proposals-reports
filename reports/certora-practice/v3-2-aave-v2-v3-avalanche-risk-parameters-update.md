# Proposal 2. Chaos Labs Risk Parameter Updates - WBTC.e on V2 and V3 Avalanche

<br>

### Voting link

[https://app.aave.com/governance/proposal/2/](https://app.aave.com/governance/proposal/2/)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-wbtc-e-on-v2-and-v3-avalanche/15824](https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-wbtc-e-on-v2-and-v3-avalanche/15824)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal freezes WBTC.e on avalanche V2 and V3 and lowers the liquidation threshold to reduce exposure to the asset by discouraging users from supplying and borrowing it. 


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xc763476c722b23e8c80260027e384a48117a199406a75692f0a7ccf1ce94e0a1](https://etherscan.io/tx/0xc763476c722b23e8c80260027e384a48117a199406a75692f0a7ccf1ce94e0a1)

```
- id: 414
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000890000000000000000000000000000000000000000000000000000000000000001000000000000000000000000401b5d0294e23637c18fcc38b1bca814cda2637c0000000000000000000000000000000000000000000000000000000000000016]
- withDelegatecalls: [false]
- startBlock: 18798764
- endBlock: 18817964
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x92b67c3c943a6674acc652eab792cd3832d095257146e24749d25b9326b04543
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/2.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/2.md)

**Payload reports**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/11.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/11.md)


<br>

### Technical analysis

We have verified that the proposal payloads correctly set the parameters for WBTC.e	on both Aave V2 and Aave V3 on Avalanche as declared in the IPFS.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. ****

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only the Avalanche V3 update utilized the config engine.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
