# Proposal 96. FEI freezing

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=96](https://app.aave.com/governance/proposal/?proposalId=96)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-risk-parameter-updates-for-ethereum-aave-v2-market/9393](https://governance.aave.com/t/arc-risk-parameter-updates-for-ethereum-aave-v2-market/9393)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

:ice_cube: freeze-asset

<br>

### Context

Given the potentially upcoming dissolution of the FEI/Tribe ecosystem, this proposal disables supplying liquidity and borrowing for [FEI](https://etherscan.io/address/0x956F47F50A910163D8BF957Cf5846D573E7f87CA) on Aave v2 Ethereum, and applies pressure on withdrawals, by reducing the supply yield to 0.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x1bd77b5a8982dd1b1cfdf337f68c3f802cf36755e21f4874b319d9a1d084b6e1](https://etherscan.io/tx/0x1bd77b5a8982dd1b1cfdf337f68c3f802cf36755e21f4874b319d9a1d084b6e1)

```
- id: 96
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xb8fe2a2104afb975240d3d32a7823a01cb74639f]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 15447358
- endBlock: 15466558
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x86fb2c1c7056f55ddfebe82b634419b2170c5cb5b981df6a0d19523dba959575
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/096.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/096.md)


<br>

### Technical analysis

The goal of the proposal is to disable as much as possible the usage of FEI into the Aave v2 Ethereum pool.

Given its usage as collateral, the only mechanism available is halting supplying of liquidity and borrowing.
In addition, to add an extra lever of pressure on withdrawals, the supply yield is set to 0, by updating the reserve factor component (% of the supply rate that gets redirected to the Aave protocol collector) to 100%. This will create a situation where depositors of FEI will not be receiving yield ("incentivising" withdrawals), which in turn will increase the utilisation of the FEI reserve, increasing the borrow rate ("incentivising" repayments).

We have verified the proposal payload does the following:
1. "Freezes" the FEI reserve (halting supplying and borrowing), by calling `freeze(addressOfFEI)` on the [pool configurator of Aave v2 Ethereum](https://etherscan.io/address/0x311Bb771e4F8952E6Da169b425E7e92d6Ac45756).
2. Update the reserve factor of the FEI reserve to 100%, by calling `setReserveFactor(addressOfFEI, 100%)`, also on the pool configurator of Aave v2 Ethereum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
