# Proposal 373. Treasury Management - TokenLogic retroactive funding

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=373](https://app.aave.com/governance/proposal/?proposalId=373)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-retrospective-funding-proposal/15324](https://governance.aave.com/t/arfc-retrospective-funding-proposal/15324)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposal approves a payment of 115'000 GHO to TokenLogic, to cover contributions to the Aave DAO the previous 6 months.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x311741c03905f081f1580b1a533b69fabda48ec001e0b5642bb8bcae1020a88d](https://etherscan.io/tx/0x311741c03905f081f1580b1a533b69fabda48ec001e0b5642bb8bcae1020a88d)

```
- id: 373
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dabad81af85554e9ae636395611c58f7ec1aaec50000000000000000000000000000000000000000000000000000000000000011]
- withDelegatecalls: [false]
- startBlock: 18593657
- endBlock: 18612857
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x663996e76ce01bdb35abd53ee9f03d15fee8d5fa9ccb4b5733a0e9eeb2549b83
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/373.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/373.md)

**Payload report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/17.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/17.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x97D74bceC48b003FCd54Ae30e595028A38e8bBA1#code#F1#L13) properly transfers 115'000 GHO from the Aave v3 Collector to the address defined as [TOKENLOGIC](https://etherscan.io/address/0x3e4A9f478C0c13A15137Fc81e9d8269F127b4B40).

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
