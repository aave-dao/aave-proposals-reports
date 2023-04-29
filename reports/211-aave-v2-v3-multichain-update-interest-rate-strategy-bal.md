# Proposal 211. Aave v2/v3 Ethereum, Polygon - update BAL rate strategies

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=211](https://app.aave.com/governance/proposal/?proposalId=211)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-bal-interest-rate-upgrade/12423](https://governance.aave.com/t/arfc-bal-interest-rate-upgrade/12423)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the interest rate strategies of BAL on Aave v2 and v3 Ethereum and Polygon.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xe7b6dd1190250f8151a9acd2e6810b6ad8fe41819f31e938c6d03b8a0f7f19f8](https://etherscan.io/tx/0xe7b6dd1190250f8151a9acd2e6810b6ad8fe41819f31e938c6d03b8a0f7f19f8)

```
- id: 211
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xeb7d3e4a6c8fb0f780e1499f9862188a65e80b14,0x5852d2e7d9e9e7a03535dd1a6c636ac7bd956070,0x158a6bc04f0828318821bae797f50b0a1299d45b,0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0,0,0,0]
- signatures: [execute(),execute(),execute(address),execute(address)]
- calldatas: [0x,0x,0x000000000000000000000000fb2a7eb134fa2d03d9a2c8fe0a9758132fe15357,0x000000000000000000000000918c0cd8291c687176029d1f2296a17e63ed3c83]
- withDelegatecalls: [true,true,true,true]
- startBlock: 17133438
- endBlock: 17152638
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x6c90c3ffa356c41df1e713cbad996d25f50e859f44d63572a973ebff0710d325
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/211.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/211.md)

**Polygon**

Payload 1:

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/211_fx_29_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/211_fx_29_0.md)

Payload 2:

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/211_fx_29_1.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/211_fx_29_1.md)

<br>

### Technical analysis

We have verified that on the non-Ethereum payloads, the proposal uses correctly the Aave cross-chain governance system to communicate with Polygon.

We have verified to all the following payloads do the same changes on the BAL rates strategies on all Aave instances:
- Base variable rate: 5%
- Variable rate slope 1: 22%
- Variable rate slope 2: 150%

**[Aave v2 Ethereum](https://etherscan.io/address/0xeb7d3e4a6c8fb0f780e1499f9862188a65e80b14#code#F4#L1)**

**[Aave v3 Ethereum](https://etherscan.io/address/0x5852d2e7d9e9e7a03535dd1a6c636ac7bd956070#code#F25#L1)**

**[Aave v2 Polygon](https://polygonscan.com/address/0xfb2a7eb134fa2d03d9a2c8fe0a9758132fe15357#code#F5#L1)**

**[Aave v3 Polygon](https://polygonscan.com/address/0x918c0cd8291c687176029d1f2296a17e63ed3c83#code#F23#L1)**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Multiple payloads used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
