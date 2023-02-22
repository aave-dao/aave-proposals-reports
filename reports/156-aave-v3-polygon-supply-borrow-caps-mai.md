# Proposal 156. Aave v3 Polygon - Supply/borrow caps update of MAI

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=156](https://app.aave.com/governance/proposal/?proposalId=156)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-increase-borrow-cap-for-mai-aave-polygon-v3/11547](https://governance.aave.com/t/arfc-increase-borrow-cap-for-mai-aave-polygon-v3/11547)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal is an update of supply and borrow caps of MAI on Aave v3 Polygon, by ACI (Aave Chan Initiative).


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xe4a41afb83ea0c175ad76c92ae3445a121d98c14c52564a5b4cd00942d32d62c](https://etherscan.io/tx/0xe4a41afb83ea0c175ad76c92ae3445a121d98c14c52564a5b4cd00942d32d62c)

```
- id: 156
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000e6e2e24643581c7118f6cf8fc30a8e236efb493e]
- withDelegatecalls: [true]
- startBlock: 16649295
- endBlock: 16668495
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xa35f0d7139e4587755589fdce946ee84f8fa201b1a8e01eab85520b35445a555
```

<br>

### Aave Seatbelt reports

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/156.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/156.md)


**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/156_fx_16_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/156_fx_16_0.md)


<br>

### Technical analysis

From a technical perspective, we have verified that the proposal payload does the following changes on Aave v3 Polygon:

- MAI supply cap changed to **1'100'000 MAI**
- MAI supply cap changed to **600'000 MAI**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
