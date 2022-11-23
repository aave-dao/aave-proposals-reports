# Proposal 123. Aave v2 Ethereum - Risk Parameter Updates. Pause UNI borrowing

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=123](https://app.aave.com/governance/proposal/?proposalId=123)

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

This proposal is an update of risk parameters on Aave v2 Ethereum by Gauntlet, specifically to pause borrowing of the UNI asset.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x39b2784fb5b7ec76b3683572c22c7590341e5cccb8555400b879e280a50cafd6](https://etherscan.io/tx/0x39b2784fb5b7ec76b3683572c22c7590341e5cccb8555400b879e280a50cafd6)

```
- id: 123
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x311bb771e4f8952e6da169b425e7e92d6ac45756]
- values: [0]
- signatures: []
- calldatas: [0xa8dc0f450000000000000000000000001f9840a85d5af5bf1d1762f925bdaddc4201f984]
- withDelegatecalls: [false]
- startBlock: 16037113
- endBlock: 16056313
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x72d7c305dc1e1ff1824fc8e23cfe603a235a8ca8b53baac86af970cda5a027a8
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/123.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/123.md)

<br>

### Technical analysis

From a technical perspective, we have verified that the calldata submitted as payload of the proposal disables borrowing of UNI on Aave v2 Ethereum (both variable and stable), by calling `disableBorrowingOnReserve()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code).

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: Payload encoded via multiple targets and calldatas, no delegatecall

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the procedure followed to submit the proposal.
