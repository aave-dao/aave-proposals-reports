# Proposal 253. Aave v2 Ethereum - Freezing of TUSD

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=253](https://app.aave.com/governance/proposal/?proposalId=253)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-freeze-tusd-on-aave-v2-ethereum-pool/13835](https://governance.aave.com/t/arfc-freeze-tusd-on-aave-v2-ethereum-pool/13835)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

:ice_cube: freeze-asset

<br>

### Context

Due to certain uncertainty surrounding the underlying asset, this proposal freezes the TUSD asset on Aave v2 Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x9ee2fba64223b7759bdc5ab6039190c7c34203e4e32ca3930148062940039d02](https://etherscan.io/tx/0x9ee2fba64223b7759bdc5ab6039190c7c34203e4e32ca3930148062940039d02)

```
- id: 253
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xddbf155eb29cebbbec67a7cf66359dd93f9f5580]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17584751
- endBlock: 17603951
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x3e42d39afde585e5c0337274a4fe907a0e6372f1925725e9d2d27faae7f1737f
```

<br>

### Aave Seatbelt report


[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/253.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/253.md)


<br>

### Technical analysis

The proposal payload interacts with the [Aave v2 Ethereum Pool Configurator](https://etherscan.io/address/0x311Bb771e4F8952E6Da169b425E7e92d6Ac45756) to call the `freezeReserve()` function TUSD, effectively freezing the asset: not allowing more supplying and borrowing.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
