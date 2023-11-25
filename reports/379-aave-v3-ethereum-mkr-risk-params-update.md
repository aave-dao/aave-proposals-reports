# Proposal 379. Aave v3 Ethereum - MKR risk parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=379](https://app.aave.com/governance/proposal/?proposalId=379)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-increase-mkr-debt-ceiling-on-v3-ethereum-11-07-2023/15406](https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-increase-mkr-debt-ceiling-on-v3-ethereum-11-07-2023/15406)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the debt ceiling parameter of MKR on Aave v3 Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xc7c43e39116638083a6aa16cfeaf564ab4b5683248f3fa7efd61840eca849657](https://etherscan.io/tx/0xc7c43e39116638083a6aa16cfeaf564ab4b5683248f3fa7efd61840eca849657)

```
- id: 379
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dabad81af85554e9ae636395611c58f7ec1aaec50000000000000000000000000000000000000000000000000000000000000015]
- withDelegatecalls: [false]
- startBlock: 18630137
- endBlock: 18649337
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x21717f4bd284ed1e6c9f93ddd02f113d821e448b1f0d7c1e4d8d52d4f0bd47a5
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/379.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/379.md)


**Payload report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/21.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/21.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xb1dA0D9bBC23A602145C9Efaf81ADD188B206d88#code#F1#L16) updates the following parameters on Aave v3 Ethereum, by using the BGD Config Engine:

MKR

- Debt ceiling: 6'000'000 USD -> **8'500'000 USD**

The proposal is consistent with the discussions on the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
