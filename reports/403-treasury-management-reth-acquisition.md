# Proposal 403. Treasury Management - rETH acquisition

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=403](https://app.aave.com/governance/proposal/?proposalId=403)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-treasury-management-add-to-reth-holding/15123](https://governance.aave.com/t/arfc-treasury-management-add-to-reth-holding/15123)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposal seeks to acquire rETH from WETH held by the Aave Ethereum Collector.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xd2c76ab702ec51482ed52b4c875fe662abe346acf66e09a9de9268a4a423abe1](https://etherscan.io/tx/0xd2c76ab702ec51482ed52b4c875fe662abe346acf66e09a9de9268a4a423abe1)

```
- id: 403
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dabad81af85554e9ae636395611c58f7ec1aaec50000000000000000000000000000000000000000000000000000000000000022]
- withDelegatecalls: [false]
- startBlock: 18784889
- endBlock: 18804089
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xf7d83414f59e9b845538f1df76d83297ab1cbcdd9f4e6c76813c61f3ecd22426
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/403.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/403.md)

**Payload report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/34.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/34.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xeeDaE6Ac41Cf7A3722eE0a220e4c932D1d58b113#code#F1#L16) does the following:
1. Transfers the WETH held by the Aave Ethereum Collector to the `AaveSwapper` contract.
2. Creates a buy order of rETH from WETH, by calling `swap()` on the AaveSwapper. The recipient of the resultant rETH will be the Aave Ethereum Collector.

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
