# Proposal 209. Aave v3 Polygon, Arbitrum - caps update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=209](https://app.aave.com/governance/proposal/?proposalId=209)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-stmatic-supply-cap-increase-polygon-v3/12606](https://governance.aave.com/t/arfc-stmatic-supply-cap-increase-polygon-v3/12606)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates supply caps of stMATIC on Aave v3 Polygon and WETH on Aave v3 Arbitrum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xe5148fb2449cea2acb17c186356439f52879452cb2fb9c687ce4ddcf932a4295](https://etherscan.io/tx/0xe5148fb2449cea2acb17c186356439f52879452cb2fb9c687ce4ddcf932a4295)

```
- id: 209
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b,0xd1b3e25fd7c8ae7caddc6f71b461b79cd4ddcfa3]
- values: [0,0]
- signatures: [execute(address),execute(address)]
- calldatas: [0x00000000000000000000000026366920975b24a89cd991a495d0d70cb8e1ba1f,0x0000000000000000000000004c68fda91bfb4683eab90017d9b76a99f2d77eed]
- withDelegatecalls: [true,true]
- startBlock: 17133249
- endBlock: 17152449
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x6b17a57b2585c7716fb784ac9f5d4c6c493db227a643698c40666c2463ecbd5c
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/209.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/209.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/209_fx_29_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/209_fx_29_0.md)

**Arbitrum**

Aave Seatbelt doesn't support Arbitrum yet.

<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Polygon and Arbitrum.
The proposals payloads do the following:

**[Polygon](https://polygonscan.com/address/0x26366920975b24a89cd991a495d0d70cb8e1ba1f#code#F22#L1)**

This payload is correctly created with the new [BGD's Aave Config Engine of Aave v3 Polygon](https://polygonscan.com/address/0xe202f2fc4b6a37ba53cfd15be42a762a645fca07#code#F18#L1) as target, doing the following changes:

- stMATIC supply cap: 21'000'000 stMATIC -> **25'000'000 stMATIC**

<br>

**[Arbitrum](https://arbiscan.io/address/0x4c68fda91bfb4683eab90017d9b76a99f2d77eed#code#F21#L1)**

This payload is also correctly created with the new [BGD's Aave Config Engine of Aave v3 Arbitrum](https://arbiscan.io/address/0x0efdfc1a940de4e7e6acc9bb801481f81b17fd20#code#F18#L1) as target, doing the following changes:

- WETH supply cap: 35'280 WETH -> **45'000 WETH**


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
