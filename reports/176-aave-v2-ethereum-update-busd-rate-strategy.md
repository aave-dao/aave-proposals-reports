# Proposal 176. Aave v2 Ethereum - update BUSD rate strategy and RF

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=176](https://app.aave.com/governance/proposal/?proposalId=176)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-busd-offboarding-plan/12170](https://governance.aave.com/t/arfc-busd-offboarding-plan/12170)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the interest rate strategy of BUSD and its Reserve Factor on Aave v2 Ethereum, as following step of the off-boarding initiated with its freezing.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xbbdeef6cc543e4d73513fdba0a88bbb4705f7dc65d79789ce7ce7a5f3d8bdeba](https://etherscan.io/tx/0xbbdeef6cc543e4d73513fdba0a88bbb4705f7dc65d79789ce7ce7a5f3d8bdeba)

```
- id: 176
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xbbf4723d70043fa338d8b519b041b476648902a6]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16797486
- endBlock: 16816686
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xe8a784a9b0773932a347ed6f74027008c088f76ac0165b97d6e78e4d46903f57
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/176.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/176.md)

**There is a infrastructural problem on Tenderly, which causes the state transitions to show erroneously. We have double checked both payload code and events emitted, and everything seems correct**

<br>

### Technical analysis

The [proposal payload](https://etherscan.io/address/0xbbf4723d70043fa338d8b519b041b476648902a6#code#F4#L1) does the following:

- Replaces the current interest rate strategy of BUSD on Aave v2 Ethereum for a [new one](https://etherscan.io/address/0x67a81df2b7faf4a324d94de9cc778704f4500478#code) with the following changes:
  - Base variable borrow: 0% -> **3%**
  - Variable borrow slope 1: 4% -> **7%**
  - Variable borrow slope 2: 100% -> **200%**
  - Stable borrow slope 1: 0% -> **7%**
  - Stable borrow slope 2: 0% -> **200%**
  - Optimal point: 80% -> **20%**

- Additionally, the proposal updates the the Reserve Factor from 10% to **99.9%**.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: Payload encoded via multiple targets and calldatas, no delegatecall

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the procedure followed to submit the proposal.
