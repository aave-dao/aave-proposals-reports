# Proposal 181. Aave v3 Ethereum - LUSD caps update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=181](https://app.aave.com/governance/proposal/?proposalId=181)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-supply-and-borrow-caps-update-lusd-v3-ethereum/12289](https://governance.aave.com/t/arfc-supply-and-borrow-caps-update-lusd-v3-ethereum/12289)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates supply and borrow caps of LUSD on Aave v3 Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xe858e1b110b04de0f0aef32a5de724acaf3d1239221521e67feeb594716da847](https://etherscan.io/tx/0xe858e1b110b04de0f0aef32a5de724acaf3d1239221521e67feeb594716da847)

```
- id: 181
- creator: 0xbc540e0729b732fb14afa240aa5a047ae9ba7df0
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x656482165fdf78f3fdd31d4ad4b518350766f3d5]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16842050
- endBlock: 16861250
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x83168013487d273f357ff2d04a8711ef9e1fb9fd440b0471726f6ef535e3426c
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/181.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/181.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x656482165fdf78f3fdd31d4ad4b518350766f3d5#code) correctly does the following caps updates affecting the LUSD asset:

- LUSD supply cap: 3'000'000 LUSD -> **6'000'000 LUSD**
- LUSD borrow cap: 1'210'000 LUSD -> **2'400'000 LUSD**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
