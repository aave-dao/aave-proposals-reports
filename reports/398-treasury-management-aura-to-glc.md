# Proposal 398. Treasury Management - Transfer AURA to GHO Liquidity Commitee (GLC)

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=398](https://app.aave.com/governance/proposal/?proposalId=398)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-treasury-management-transfer-aura-to-glc-safe/15669](https://governance.aave.com/t/arfc-treasury-management-transfer-aura-to-glc-safe/15669)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposal transfers the AURA held by the Aave DAO in the Aave Ethereum Collector to the GHO Liquidity Commitee (GLC), to vote for GHO incentives in the Aura platform.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x0fd63d1a08a4ac7926185886df8ef2a71d9ebd0d2af26c2b4f504400f8ad63d4](https://etherscan.io/tx/0x0fd63d1a08a4ac7926185886df8ef2a71d9ebd0d2af26c2b4f504400f8ad63d4)

```
- id: 398
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dabad81af85554e9ae636395611c58f7ec1aaec50000000000000000000000000000000000000000000000000000000000000020]
- withDelegatecalls: [false]
- startBlock: 18743678
- endBlock: 18762878
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xf73330ab5bbc2f9de75ecc62cc9facf2d51d14689f6fbcb8a935eed53d5b357d
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/398.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/398.md)

**Payload reports**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/32.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/32.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x312C428a84102B76ca9D38027Ea506f542120965#code#F1#L15) properly transfers all the AURA available balance from the Aave Ethereum Collector to the [GHO Liquidity Commitee](https://etherscan.io/address/0x205e795336610f5131Be52F09218AF19f0f3eC60), labelled as `GLC_SAFE`.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
