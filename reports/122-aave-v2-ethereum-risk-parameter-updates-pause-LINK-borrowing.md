# Proposal 122. Aave v2 Ethereum - Risk Parameter Updates. Pause LINK borrowing

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=122](https://app.aave.com/governance/proposal/?proposalId=122)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-risk-parameter-recommendations-for-aave-v2-eth-2022-11-22/10757](https://governance.aave.com/t/arc-risk-parameter-recommendations-for-aave-v2-eth-2022-11-22/10757)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal is an update of risk parameters on Aave v2 Ethereum by Gauntlet, specifically to pause borrowing of the LINK asset.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x022f2bab36b4cc4651b0de42023a914eff2372f342ff8cad950a8054e3033af4](https://etherscan.io/tx/0x022f2bab36b4cc4651b0de42023a914eff2372f342ff8cad950a8054e3033af4)

```
- id: 122
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x311bb771e4f8952e6da169b425e7e92d6ac45756]
- values: [0]
- signatures: []
- calldatas: [0xa8dc0f45000000000000000000000000514910771af9ca656af840dff83e8264ecf986ca]
- withDelegatecalls: [false]
- startBlock: 16037108
- endBlock: 16056308
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x156304a338a9c71cca4be6ce621f0c7550ba96f8dbfde98dde90af622a5fa0df
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/122.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/122.md)

<br>

### Technical analysis

From a technical perspective, we have verified that the calldata submitted as payload of the proposal disables borrowing of LINK on Aave v2 Ethereum (both variable and stable), by calling `disableBorrowingOnReserve()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code).

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: Payload encoded via multiple targets and calldatas, no delegatecall

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the procedure followed to submit the proposal.
