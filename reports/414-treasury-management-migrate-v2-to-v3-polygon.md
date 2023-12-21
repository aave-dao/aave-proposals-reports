# Proposal 414. Treasury Management - Migrate all Polygon Collector v2 aTokens to v3

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=414](https://app.aave.com/governance/proposal/?proposalId=414)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-migrate-consolidate-polygon-treasury/12248](https://governance.aave.com/t/arfc-migrate-consolidate-polygon-treasury/12248)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposal migrates all assets of the Aave Polygon Collector held in v2 aTokens to v3 aTokens, apart from BAL and CRV.


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

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/414.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/414.md)

**Payload reports**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/38.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/38.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://polygonscan.com/address/0x31B7F31dcCF8E8127a6f1619e6624A2a5Ef6713B#code#F1#L45) properly migrates all Aave v2 Polygon (apart from aBAL and aCRV) available balance from the Aave Polygon Collector into Aave v3 Polygon.

Additionally, the balances of USDC.e (bridged) and WMATIC of the Aave Polygon Collector are also migrated to Aave v3 Polygon.

We have confirmed the recipient of all the migrations is effectively the Aave Polygon Collector.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
