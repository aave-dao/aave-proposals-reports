# Proposal 374. Treasury Management - rETH acquisition

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=374](https://app.aave.com/governance/proposal/?proposalId=374)

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

This proposal seeks to acquire rETH from WETH and aWETH (v2 and v3) held by the Aave Ethereum Collector.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x90c3330cb5c5be00a63d4324aa02b89aa5a22eb20b4699b309d2cac55f0abe6b](https://etherscan.io/tx/0x90c3330cb5c5be00a63d4324aa02b89aa5a22eb20b4699b309d2cac55f0abe6b)

```
- id: 374
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dabad81af85554e9ae636395611c58f7ec1aaec5000000000000000000000000000000000000000000000000000000000000000f]
- withDelegatecalls: [false]
- startBlock: 18593667
- endBlock: 18612867
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x2187a22d1c0a9eba2d112f38b51ad1716a49842ecd2d8efcb146876c20bfb848
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/374.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/374.md)

**Payload report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/15.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/15.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xB08b75BaAC19FAcd43e643af10B35E5cA3527F5F#code#F1#L33) does the following:
1. Transfers the WETH held by the Aave Ethereum Collector to the `AaveSwapper` contract.
2. Redeems aWETH v2 and v3 held by the same Collector, and transfers the resultant WETH to the `AaveSwapper`. As described in the proposal, 100 aWETH v3 is left on the Collector.
3. Creates a buy order of rETH from WETH, by calling `swap()` on the AaveSwapper. The recipient of the resultant rETH will be the Aave Ethereum Collector.

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
