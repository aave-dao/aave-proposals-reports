# Proposal 151. Aave v3/v2 Polygon and Aave v2 Ethereum - update BAL interest rate strategies

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=151](https://app.aave.com/governance/proposal/?proposalId=151)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-bal-interest-rate-curve-upgrade/10484/10](https://governance.aave.com/t/arfc-bal-interest-rate-curve-upgrade/10484/10)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the interest rate strategy for BAL on the Aave v2/v3 Polygon and Aave v2 Ethereum pools, together with the borrow cap on Aave v3 Polygon.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xe10db4310288b3a473704d72f3ad116aeaf539d52bbf47fbbc399933b3f4958e](https://etherscan.io/tx/0xe10db4310288b3a473704d72f3ad116aeaf539d52bbf47fbbc399933b3f4958e)

```
- id: 151
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x3b6532efb7a60711f8f3fa77a589a726c836f4cf,0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0,0]
- signatures: [execute(),execute(address)]
- calldatas: [0x,0x00000000000000000000000098bc9dfa3cecb37f1bdeadc6e774d39082756b19]
- withDelegatecalls: [true,true]
- startBlock: 16549271
- endBlock: 16568471
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x4f3905da8ccd469111977b3057fa544bec56880a6039c7977dbc68aeaba48536
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/151.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/151.md)



**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/151_fx_12_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/151_fx_12_0.md)

<br>

### Technical analysis

This proposal has 2 target networks: Ethereum and Polygon, so we have analyzed the changes applied separately.

**Ethereum**

We have verified [the proposal payload](https://etherscan.io/address/0x3b6532efb7a60711f8f3fa77a589a726c836f4cf#code) just updates the interest rate strategy for BAL, setting a new one with the following parameters:

- Optimal point: 80%
- Base variable borrow rate: 3%
- Variable borrow slope 1: 14%
- Variable borrow slope 2: 150%

These parameters are the same as defined on the governance forum and Snapshot.

**Polygon**

The proposal payload properly interacts with the Aave cross-chain governance system, via the the [CrosschainForwarderPolygon](https://etherscan.io/address/0x158a6bC04F0828318821baE797f50B0A1299d45b#code), to later execute the [proposal payload on Polygon](https://polygonscan.com/address/0x98bc9dfa3cecb37f1bdeadc6e774d39082756b19#code) doing the following:

- Update the borrow cap of BAL from 156'530 BAL to 256'140 BAL, by calling the [Pool Configurator contract of Aave v3 Polygon](https://polygonscan.com/address/0x8145eddDf43f50276641b55bd3AD95944510021E).
- Update the interest rate strategies of BAL on both Aave v2 and v3 Polygon with new ones with the following parameters:
  - Optimal point: 80%
  - Base variable borrow rate: 3%
  - Variable borrow slope 1: 14%
  - Variable borrow slope 2: 150%

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
