# Proposal 162. BUSD freezing on Aave v2 Ethereum

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=162](https://app.aave.com/governance/proposal/?proposalId=162)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-freeze-busd-on-aave-v2/11842](https://governance.aave.com/t/arfc-freeze-busd-on-aave-v2/11842)

<br>

## BGD analysis

<br>

### Proposal types

:ice_cube: freeze-asset

<br>

### Context

Given the upcoming halting of BUSD minting, this proposal freezes BUSD on Aave v2 Ethereum, stopping new deposits and borrowings, but keeping all other dynamics (repayment, liquidation).

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x40efa789f79416a27d9978acf003ea48dfe75f087c14c73638d9784c4667adb9](https://etherscan.io/tx/0x40efa789f79416a27d9978acf003ea48dfe75f087c14c73638d9784c4667adb9)

```
- id: 162
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9c4bf756e2d8da301121b036958f6b3fcd0fe801]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16685056
- endBlock: 16704256
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x1b90a1c2218867611b3d705e42b65c4a54a0e72bf5d23d20cc292d47c05a1568
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/162.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/162.md)


<br>

### Technical analysis

The [proposal payload](https://etherscan.io/address/0x9c4bf756E2d8dA301121b036958f6B3fcd0FE801#code#F4#L1) simply interacts with the [PoolConfigurator](https://etherscan.io/address/0x311Bb771e4F8952E6Da169b425E7e92d6Ac45756) of Aave v2 Ethereum to freeze BUSD by calling the `freezeReserve()` function.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
