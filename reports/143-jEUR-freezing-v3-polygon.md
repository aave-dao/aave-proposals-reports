# Proposal 143. Aave v3 Polygon - Freezing of jEUR

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=143](https://app.aave.com/governance/proposal/?proposalId=143)

<br>

### Governance forum discussion

[https://governance.aave.com/t/jeur-incident-plan-of-action/11379](https://governance.aave.com/t/jeur-incident-plan-of-action/11379)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

:ice_cube: freeze-asset

<br>

### Context

Following an exploit on the Midas protocol affecting jEUR, this proposal freezes the jEUR asset on Aave v3 Polygon.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x567fc957cbdeb0deca8630c6cc1bfd0dcffca2d1be881e21c8b8a73b14021871](https://etherscan.io/tx/0x567fc957cbdeb0deca8630c6cc1bfd0dcffca2d1be881e21c8b8a73b14021871)

```
- id: 143
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000165e90bd0a41d08fa1891ccdcee315d7b83b3419]
- withDelegatecalls: [true]
- startBlock: 16442002
- endBlock: 16461202
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x0baa1d8fa1dbcd7a15276f668b234f9847ba2848f9aa6a4b79eaa6d927b92b8e
```

<br>

### Aave Seatbelt report

**Ethereum**
[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/143.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/143.md)

**Polygon**
[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/143_fx_11_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/143_fx_11_0.md)


<br>

### Technical analysis

This is a cross-chain governance proposal, with [its payload](https://polygonscan.com/address/0x165e90bd0a41d08fa1891ccdcee315d7b83b3419#code) interacting with the Aave v3 Polygon by calling `setReserveFreeze()` on the [Pool Configurator contract](https://polygonscan.com/address/0x8145eddDf43f50276641b55bd3AD95944510021E).

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD wrote the payload.

:x: With BGD writing the payload, at least another party reviewed it.
