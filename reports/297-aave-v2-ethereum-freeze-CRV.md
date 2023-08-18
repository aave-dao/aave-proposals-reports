# Proposal 297. Aave v2 Ethereum - Freezing of CRV

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=297](https://app.aave.com/governance/proposal/?proposalId=297)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-gauntlet-recommendation-on-freezing-crv-for-aave-v2-ethereum/14428](https://governance.aave.com/t/arfc-gauntlet-recommendation-on-freezing-crv-for-aave-v2-ethereum/14428)

<br>

## BGD analysis

<br>

### Proposal types

:ice_cube: freeze-asset

<br>

### Context

Following a de-risking plan from risk providers, this proposal freezes CRV on Aave v2 Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x40dd067d88bb53adc9b55d582e07bb9b24ddba3db369238c17c4aa936d05c6a5](https://etherscan.io/tx/0x40dd067d88bb53adc9b55d582e07bb9b24ddba3db369238c17c4aa936d05c6a5)

```
- id: 297
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x311bb771e4f8952e6da169b425e7e92d6ac45756]
- values: [0]
- signatures: [freezeReserve(address)]
- calldatas: [0x000000000000000000000000d533a949740bb3306d119cc777fa900ba034cd52]
- withDelegatecalls: [false]
- startBlock: 17923213
- endBlock: 17942413
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x1c51cac5e659d29de16da2c0a97ec51a928bb2d9f3d7aba6a53335436e535086
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/297.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/297.md)


<br>

### Technical analysis

The proposal payload (submitted via calldata) interacts with the [Aave v2 Ethereum Pool Configurator](https://etherscan.io/address/0x311Bb771e4F8952E6Da169b425E7e92d6Ac45756) to call the `freezeReserve()` function on CRV, effectively allowing more supplying and borrowing (already disabled).

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the payload before the proposal was submitted.

:x: Only one payload used via delegatecall

:question: BGD reviewed the procedure followed to submit the proposal.