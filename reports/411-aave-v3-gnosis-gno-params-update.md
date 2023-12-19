# Proposal 411. Aave v3 Gnosis - GNO parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=411](https://app.aave.com/governance/proposal/?proposalId=411)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-update-gno-risk-parameters-on-aave-v3-gnosis-pool/15613](https://governance.aave.com/t/arfc-update-gno-risk-parameters-on-aave-v3-gnosis-pool/15613)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal enables GNO for borrowing and updates its borrow cap and reserve factor, on Aave v3 Gnosis.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x6be9a60ff38e48fa8abf13b066df826345c472434ae7c62b04a29759675932ed](https://etherscan.io/tx/0x6be9a60ff38e48fa8abf13b066df826345c472434ae7c62b04a29759675932ed)

```
- id: 411
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x000000000000000000000000000000000000000000000000000000000000006400000000000000000000000000000000000000000000000000000000000000010000000000000000000000009a1f491b86d09fc1484b5fab10041b189b60756b0000000000000000000000000000000000000000000000000000000000000001]
- withDelegatecalls: [false]
- startBlock: 18797556
- endBlock: 18816756
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x3eebf43ac403bb9da7d9191d52cf0ea21f8a1ff988f83501dab7881b93b309e8
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/411.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/411.md)


**Payload report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/1.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/1.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://gnosisscan.io/address/0xc3785b4249699f8d522ea7997e59028010b21c8c#code#F1#L16) updates the following parameters on Aave v3 Gnosis, by using the BGD Config Engine:

GNO

- Enables the asset for borrowing.
- The interest rate strategy is configured the following way:
  - Base variable borrow: 0%
  - Variable borrow slope 1: 15%
  - Variable borrow slope 2: 80%
  - Optimal point: 80%
- Borrow cap: No cap -> **1'100 GNO**
- Reserve factor: 15% -> **20%**

<br>

The proposal is consistent with the discussions on the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
