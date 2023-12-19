# Proposal 412. Treasury Management - Transfer CRV and aCRV (v2/v3) to GHO Liquidity Commitee (GLC)

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=412](https://app.aave.com/governance/proposal/?proposalId=412)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-deploy-acrv-crv-to-vecrv/11628](https://governance.aave.com/t/arfc-deploy-acrv-crv-to-vecrv/11628)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposal transfers all the CRV (redeeming aCRV (v2/v3) too) held by the Aave DAO in the Aave Ethereum Collector to the GHO Liquidity Commitee (GLC), for usage in the incentivisation of GHO on the Curve platform, via StakeDAO.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xe80efe71357574155c123b43f08d32bc32191a3d7a8593787749c5b491f7c3ae](https://etherscan.io/tx/0xe80efe71357574155c123b43f08d32bc32191a3d7a8593787749c5b491f7c3ae)

```
- id: 412
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dabad81af85554e9ae636395611c58f7ec1aaec50000000000000000000000000000000000000000000000000000000000000026]
- withDelegatecalls: [false]
- startBlock: 18797804
- endBlock: 18817004
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x522201994687772117e9786a7450b39dd02e112e3ec3828fce2342fde71f3f1e
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/412.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/412.md)

**Payload reports**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/38.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/38.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x66c6ba442D5947007263238bA8deDDE2Dc9fd855#code#F1#L16) properly transfers all the CRV available balance from the Aave Ethereum Collector to the [GHO Liquidity Commitee](https://etherscan.io/address/0x205e795336610f5131Be52F09218AF19f0f3eC60), labelled as `GLC_SAFE`.

Before that transfer, the whole balance of aCRV v2/v3 is redeemed, to also send the proceeds of it.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
