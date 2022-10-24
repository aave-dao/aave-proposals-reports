# Proposal 111. Aave v2 Ethereum - Risk Parameter Updates 2022-10-21

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=111](https://app.aave.com/governance/proposal/?proposalId=111)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-price-manipulation-implications-on-aave-october-2022/10262](https://governance.aave.com/t/arc-price-manipulation-implications-on-aave-october-2022/10262)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal is a periodic update by Gauntlet concerning risk parameters on Aave v2 Ethereum.

It includes lowering of liquidations thresholds which technically could cause liquidation of positions. Gauntlet has communicated us that at the current moment there is no meaningful user positions to be affected by the parameters update, liquidation-wise.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x0b5d399554bda23ef88395de50b9924be1659d7fa3c3cbe2c53c5743d0a3a319](https://etherscan.io/tx/0x0b5d399554bda23ef88395de50b9924be1659d7fa3c3cbe2c53c5743d0a3a319)

```
- id: 111
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756]
- values: [0,0,0,0,0,0,0,0,0]
- signatures: [,,,,,,,,]
- calldatas: [0x7c4e560b0000000000000000000000000d8775f648430679a709e98d2b0cb6250d2887ef00000000000000000000000000000000000000000000000000000000000019640000000000000000000000000000000000000000000000000000000000001b5800000000000000000000000000000000000000000000000000000000000029fe,0x7c4e560b0000000000000000000000004e3fbd56cd56c3e72c1403e103b45db9da5b9d2b0000000000000000000000000000000000000000000000000000000000000dac00000000000000000000000000000000000000000000000000000000000011940000000000000000000000000000000000000000000000000000000000002a62,0x7c4e560b000000000000000000000000e41d2489571d322189246dafa5ebde1f4699f498000000000000000000000000000000000000000000000000000000000000157c000000000000000000000000000000000000000000000000000000000000196400000000000000000000000000000000000000000000000000000000000029fe,0xa8dc0f45000000000000000000000000ba100000625a3754423978a60c9317c58a424e3d,0xa8dc0f450000000000000000000000000d8775f648430679a709e98d2b0cb6250d2887ef,0xa8dc0f450000000000000000000000004e3fbd56cd56c3e72c1403e103b45db9da5b9d2b,0xa8dc0f450000000000000000000000001494ca1f11d487c2bbe4543e90080aeba4ba3c2b,0xa8dc0f45000000000000000000000000408e41876cccdc0f92210600ef50372656052a38,0xa8dc0f45000000000000000000000000e41d2489571d322189246dafa5ebde1f4699f498]
- withDelegatecalls: [false,false,false,false,false,false,false,false,false]
- startBlock: 15798685
- endBlock: 15817885
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xb86e0c2d284903bb3fa3fc989dc249fc12f93609c0851d6a9a1b7738bee477fa
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/111.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/111.md)

<br>

### Technical analysis

From a technical perspective, we have verified that the calldata submitted as payload of the proposal does the following:

1. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for BAL, with the following changes:
    - **Disabling borrowing**
2. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for BAT, with the following changes:
    - LTV: **75% -> 65%**
    - Liquidation Threshold: **80% -> 70%**
    - **Disabling borrowing**
3. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for CVX, with the following changes:
    - LTV: **45% -> 35%**
    - Liquidation Threshold: **60% -> 45%**
    - **Disabling borrowing**
4. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for DPI, with the following changes:
    - **Disabling borrowing**
5. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for REN, with the following changes:
    - **Disabling borrowing**
6. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for ZRX, with the following changes:
    - LTV: **65% -> 55%**
    - Liquidation Threshold: **75% -> 65%**
    - **Disabling borrowing**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: Payload encoded via multiple targets and calldatas, no delegatecall

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the procedure followed to submit the proposal.
