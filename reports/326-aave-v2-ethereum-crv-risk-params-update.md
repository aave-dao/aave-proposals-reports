# Proposal 326. Aave v2 Ethereum - CRV risk parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=326](https://app.aave.com/governance/proposal/?proposalId=326)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-crv-aave-v2-ethereum-lt-reduction-09-19-2023/14890](https://governance.aave.com/t/arfc-crv-aave-v2-ethereum-lt-reduction-09-19-2023/14890)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal reduces the Liquidation Threshold (LT) of CRV by 2% on Aave v2 Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xcad64371834aa7f230b8f9a03a2b20c88cf4bad75cb17bda262e00146c821502](https://etherscan.io/tx/0xcad64371834aa7f230b8f9a03a2b20c88cf4bad75cb17bda262e00146c821502)

```
- id: 326
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x77cd8ac33c5ccdae345c223bcbd0e2d45cb430af]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 18199928
- endBlock: 18219128
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xfea70c498653dd3f664e41a129a7c43222ba79061846cc67bac3fb6cee674879
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/326.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/326.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x77cd8ac33c5ccdae345c223bcbd0e2d45cb430af#code#F1#L13) properly reduces the LT of CRV to **45%** (from 47%) on Aave v2 Ethereum, by interacting with the Pool Configurator contract.

The proposal is consistent with the discussions on the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
