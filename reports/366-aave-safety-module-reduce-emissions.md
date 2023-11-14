# Proposal 365. Aave Safety Module - Reduce AAVE emissions

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=366](https://app.aave.com/governance/proposal/?proposalId=366)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-treasury-management-amend-safety-module-aave-emissions/14936](https://governance.aave.com/t/arfc-treasury-management-amend-safety-module-aave-emissions/14936)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal reduces the AAVE rewards emission rate on both stkAAVE and stkABPT from 550 AAVE/day to 385 AAVE/day.

**THE TARGET EXECUTOR OF THE PROPOSAL DOESN'T HAVE ENOUGH PERMISSIONS, SO EXECUTION WILL ALWAYS REVERT. Even if this is not adding any danger to the protocol, we have communicated the proposal creator about this, as they will need to re-submit it**.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x3de8df0fdfc35d99c61d44e654df2ddf47dd0f1e1fe19a29285883864f013318](https://etherscan.io/tx/0x3de8df0fdfc35d99c61d44e654df2ddf47dd0f1e1fe19a29285883864f013318)

```
- id: 366
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dabad81af85554e9ae636395611c58f7ec1aaec5000000000000000000000000000000000000000000000000000000000000000c]
- withDelegatecalls: [false]
- startBlock: 18548923
- endBlock: 18568123
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xed97482927ce520944c9904a792d63f37d9941ec95ae8a1f8f6ae6c40d8d2cca
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/366.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/366.md)

**Payloads report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/12.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/12.md)

<br>

### Technical analysis


**As we commented before, the proposal will revert due to a lack of permissions**
