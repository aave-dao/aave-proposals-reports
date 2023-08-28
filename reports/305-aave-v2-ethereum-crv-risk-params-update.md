# Proposal 305. Aave v2 Ethereum - CRV risk parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=305](https://app.aave.com/governance/proposal/?proposalId=305)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-crv-aave-v2-ethereum-lt-reduction-08-21-2023/14589](https://governance.aave.com/t/arfc-crv-aave-v2-ethereum-lt-reduction-08-21-2023/14589)

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

Transaction: [https://etherscan.io/tx/0x0f2e228106295df9bfc9420aa824e183a441c6a25a6bb771e22e6012326b006d](https://etherscan.io/tx/0x0f2e228106295df9bfc9420aa824e183a441c6a25a6bb771e22e6012326b006d)

```
- id: 305
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x3ed5ca03cbd02a47f3193717f1de723bb69f48fa]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17986627
- endBlock: 18005827
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x26d4b0230da0fde5fde20251a9d2a7dc2e20b26d1549a296e165fdc0bcca4489
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/305.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/305.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x3ed5ca03cbd02a47f3193717f1de723bb69f48fa#code#F1#L13) properly reduces the LT of CRV to **47%** (from 49%) on Aave v2 Ethereum, by interacting with the Pool Configurator contract.

The proposal is consistent with the discussions on the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
