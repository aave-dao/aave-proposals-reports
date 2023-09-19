# Proposal 323. Aave v3 Ethereum - GHO interest rate strategy update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=323](https://app.aave.com/governance/proposal/?proposalId=323)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-increase-gho-borrow-rate/14612](https://governance.aave.com/t/arfc-increase-gho-borrow-rate/14612)

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

Transaction: [https://etherscan.io/tx/0xdd6112e9e548875d4175385938cb5abe92a3eaeea7f2125171477b39ab0678ed](https://etherscan.io/tx/0xdd6112e9e548875d4175385938cb5abe92a3eaeea7f2125171477b39ab0678ed)

```
- id: 323
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x77c2bf7d387d4d0c54dad4221764f0ac0c289d24]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 18148589
- endBlock: 18167789
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xb6d3d8b8aeaca0cb411a1eda57ba847a3ed346ecfe9e01367ed4ee62c369b426
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/323.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/323.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x77c2bf7d387d4d0c54dad4221764f0ac0c289d24#code#F1#L12) properly updates the GHO interest rate strategy with [this one](https://etherscan.io/address/0x9210E5477dCA5bdF579ef0E1Ae84F9E823a5A3bA#code#F1#L15).

This will change the GHO (fixed) rate to 2.5%, from the current 1.5%.

The proposal is consistent with the discussions on the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
