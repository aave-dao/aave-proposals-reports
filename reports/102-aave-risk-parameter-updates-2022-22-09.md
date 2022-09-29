# Proposal 102. Aave v2 Ethereum - Risk Parameter Updates 2022/09/22

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=102](https://app.aave.com/governance/proposal/?proposalId=102)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-risk-parameter-updates-for-aave-v2-and-aave-arc-fireblocks-2022-09-22/9983](https://governance.aave.com/t/arc-risk-parameter-updates-for-aave-v2-and-aave-arc-fireblocks-2022-09-22/9983)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal is a periodic update by Gauntlet concerning risk parameters on Aave v2 Ethereum.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xe8dc3d5ea4fcf90391fc96de9ed89bd1aa4b39e669695ec628a31a4cc3b49806](https://etherscan.io/tx/0xe8dc3d5ea4fcf90391fc96de9ed89bd1aa4b39e669695ec628a31a4cc3b49806)

```
- id: 102
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756,0x311bb771e4f8952e6da169b425e7e92d6ac45756]
- values: [0,0,0,0]
- signatures: [,,,]
- calldatas: [0x7c4e560b000000000000000000000000a0b86991c6218b36c1d19d4a2e9eb0ce3606eb4800000000000000000000000000000000000000000000000000000000000021fc00000000000000000000000000000000000000000000000000000000000022c400000000000000000000000000000000000000000000000000000000000028d2,0x7c4e560b0000000000000000000000007fc66500c84a76ad7e9c93437bfc5ac33e2ddae900000000000000000000000000000000000000000000000000000000000019c80000000000000000000000000000000000000000000000000000000000001c8400000000000000000000000000000000000000000000000000000000000029fe,0x7c4e560b0000000000000000000000001f9840a85d5af5bf1d1762f925bdaddc4201f98400000000000000000000000000000000000000000000000000000000000019640000000000000000000000000000000000000000000000000000000000001e140000000000000000000000000000000000000000000000000000000000002a94,0x7c4e560b000000000000000000000000c02aaa39b223fe8d0a0e5c4f27ead9083c756cc2000000000000000000000000000000000000000000000000000000000000203a00000000000000000000000000000000000000000000000000000000000021980000000000000000000000000000000000000000000000000000000000002904]
- withDelegatecalls: [false,false,false,false]
- startBlock: 15627550
- endBlock: 15646750
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x55588a2d7fa9c28509ea269bd1245ce25dbe2dffc45ae905e2d22d5862648ba9
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/102.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/102.md)

<br>

### Technical analysis

From a technical perspective, we have verified that the calldata submitted as payload of the proposal does the following:

1. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for UNI, with the following changes:
    - LTV: **60% -> 65%**
    - Liquidation Threshold: **75% -> 77%**
    - Liquidation Bonus: 9% -> 9%
2. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for AAVE, with the following changes:
    - LTV: **62.5% -> 66%**
    - Liquidation Threshold: **70% -> 73%**
    - Liquidation Bonus: 7.5% -> 7.5%
3. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for USDC, with the following changes:
    - LTV: **85.5% -> 87%**
    - Liquidation Threshold: **88% -> 89%**
    - Liquidation Bonus: 4.5% -> 4.5%
4. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://etherscan.io/address/0x311bb771e4f8952e6da169b425e7e92d6ac45756#code) for WETH, with the following changes:
    - LTV: 82.5% -> 82.5%
    - Liquidation Threshold: **85% -> 86%**
    - Liquidation Bonus: 5% -> 5%

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: Payload encoded via multiple targets and calldatas, no delegatecall

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the payload before the proposal was submitted.

:x: BGD reviewed the procedure followed to submit the proposal.
