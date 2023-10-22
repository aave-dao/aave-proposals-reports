# Proposal 349. Aave v3 Ethereum - GHO interest rate strategy update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=349](https://app.aave.com/governance/proposal/?proposalId=349)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-further-increase-gho-borrow-rate/15053](https://governance.aave.com/t/arfc-further-increase-gho-borrow-rate/15053)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the interest rate strategy of GHO on Aave v3 Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x0aeafbb1ad6449df0c18efb857d9eedb7edf337a46d7b592ee4037ac24198c37](https://etherscan.io/tx/0x0aeafbb1ad6449df0c18efb857d9eedb7edf337a46d7b592ee4037ac24198c37)

```
- id: 349
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x46d0655ad49a7b5dda47fd68a60240a713eb1b09]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 18386901
- endBlock: 18406101
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x0c313791237543bbe3671f67fed9c33eae3f7f06a403102469c94ffcdc5efac3
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/349.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/349.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x46d0655ad49a7b5dda47fd68a60240a713eb1b09#code#F1#L12) properly updates the GHO interest rate strategy with [this one](https://etherscan.io/address/0x1255fc8dc8e76761995acf544eea54f1b7fb0459#code).

This will change the GHO (fixed) rate to 3%, from the current 2.5%.

The proposal is consistent with the discussions on the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
