# Proposal 256. Aave v2 Ethereum - TUSD risk parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=256](https://app.aave.com/governance/proposal/?proposalId=256)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-gauntlet-recommendation-on-tusd-for-aave-v2-ethereum/13727](https://governance.aave.com/t/arfc-gauntlet-recommendation-on-tusd-for-aave-v2-ethereum/13727)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates multiple risk parameters of the TUSD asset on Aave v2 Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xceb26d258faf27b79f08957b2c3ac30b2ffb6c1c18db4b6c322c34dcd693cbbc](https://etherscan.io/tx/0xceb26d258faf27b79f08957b2c3ac30b2ffb6c1c18db4b6c322c34dcd693cbbc)

```
- id: 256
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x311bb771e4f8952e6da169b425e7e92d6ac45756]
- values: [0]
- signatures: [configureReserveAsCollateral(address,uint256,uint256,uint256)]
- calldatas: [0x0000000000000000000000000000000000085d4780b73119b644ae5ecd22b3760000000000000000000000000000000000000000000000000000000000001d4c0000000000000000000000000000000000000000000000000000000000001e460000000000000000000000000000000000000000000000000000000000002904]
- withDelegatecalls: [false]
- startBlock: 17587387
- endBlock: 17606587
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x5ad00ebf0e170757dbb0559d21dab778084108f6388d548471a424137c238c36
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/256.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/256.md)


<br>

### Technical analysis

We have verified the proposal payload (encoded via calldata) properly changes the following risk parameters of TUSD on Aave v2 Ethereum:

TUSD
- LTV: 80% -> **75%**
- Liquidation Threshold: 82.5% -> **77.5%**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: Payload encoded via multiple targets and calldatas, no delegatecall

:x: BGD reviewed the payload before the proposal was submitted.

:x: BGD reviewed the procedure followed to submit the proposal.
