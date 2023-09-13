# Proposal 316. Treasury Management - Gas Rebate delegates

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=316](https://app.aave.com/governance/proposal/?proposalId=316)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-quarterly-gas-rebate-distribution-august-2023/14680](https://governance.aave.com/t/arfc-quarterly-gas-rebate-distribution-august-2023/14680)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposal reimburses different Aave recognized delegates for the gas cost incurred while participating in governance.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xafcf9bdea60d0ead28ec8cd2a018de653488733af99dc4c60f17be1d7a6d1370](https://etherscan.io/tx/0xafcf9bdea60d0ead28ec8cd2a018de653488733af99dc4c60f17be1d7a6d1370)

```
- id: 316
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xe0ecde7e3bf61f09a5c745154c736de85a290d4a]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 18099201
- endBlock: 18118401
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x90554befe3e2ec212b5d7f6ddc5909e6502e93fdb542ec60e192b4dacd891ba0
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/316.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/316.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xe0ecde7e3bf61f09a5c745154c736de85a290d4a#code#F1#L47) properly transfers an aggregated of 2.7 ETH to different addresses of delegates following these steps:

1. Withdraw WETH from the Aave Ethereum Collector.
2. Unwrap WETH to ETH.
3. Send the individual amounts to the different delegates' addresses.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
