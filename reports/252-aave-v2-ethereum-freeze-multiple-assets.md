# Proposal 252. Aave v2 Ethereum - Freezing multiple assets that should be migrated to v3

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=252](https://app.aave.com/governance/proposal/?proposalId=252)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-v2-to-v3-migration-next-steps/13701](https://governance.aave.com/t/arfc-chaos-labs-v2-to-v3-migration-next-steps/13701)

<br>

## BGD analysis

<br>

### Proposal types

:ice_cube: freeze-asset

<br>

### Context

In order to incentivize a migration to Aave v3 Ethereum, this proposal freezes multiple assets listed in both Aave versions on Ethereum: SNX, ENS, LINK, MKR, UNI and 1INCH.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xe13424ec0a8834b3c3d3089431653e22115b39814475ab1dadcd3c58e5f971ee](https://etherscan.io/tx/0xe13424ec0a8834b3c3d3089431653e22115b39814475ab1dadcd3c58e5f971ee)

```
- id: 252
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xc1a6036b2915c0c151d8761b5d70e51726ba306f]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17544920
- endBlock: 17564120
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x9b5e945ae783f140196ba8709c70eb6c5cbb4e5ab978fb926dcadb8931d7f18b
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/252.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/252.md)


<br>

### Technical analysis

The proposal payload interacts with the [Aave v2 Ethereum Pool Configurator](https://etherscan.io/address/0x311Bb771e4F8952E6Da169b425E7e92d6Ac45756) to call the `freezeReserve()` function on 1INCH, ENS, LINK, MKR, SNX and UNI, effectively freezing those assets: not allowing more supplying and borrowing.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.