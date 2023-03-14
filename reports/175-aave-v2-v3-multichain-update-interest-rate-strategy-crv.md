# Proposal 175. Aave v2 Ethereum, Polygon and v3 Polygon - update CRV rate strategy

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=175](https://app.aave.com/governance/proposal/?proposalId=175)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-crv-interest-rate-curve-upgrade/11337](https://governance.aave.com/t/arfc-crv-interest-rate-curve-upgrade/11337)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the interest rate strategies for CRV on Aave v2 Ethereum and Polygon, together with Aave v3 Polygon.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x5d15de218779cb69edb2b930dcc7e92ab22ec27bbbdbe52ca2ce12f61e870d1b](https://etherscan.io/tx/0x5d15de218779cb69edb2b930dcc7e92ab22ec27bbbdbe52ca2ce12f61e870d1b)

```
- id: 175
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xbacbe678e2c59343024fd5755262c7b0f77867d1,0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0,0]
- signatures: [execute(),execute(address)]
- calldatas: [0x,0x0000000000000000000000003b6532efb7a60711f8f3fa77a589a726c836f4cf]
- withDelegatecalls: [true,true]
- startBlock: 16792219
- endBlock: 16811419
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x5850c334a550896520dd390da343896affe8cbe21d5708c013e3f42c11b31703
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/175.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/175.md)

**There is a infrastructural problem on Tenderly, which causes the state transitions to show erroneously. We have double checked both payload code and events emitted, and everything seems correct**

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/175_fx_17_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/175_fx_17_0.md)

<br>

### Technical analysis

The proposal payloads do the following:

**[Ethereum](https://etherscan.io/address/0xbacbe678e2c59343024fd5755262c7b0f77867d1#code#F3#L14)**

Replaces the current interest rate strategy of CRV on Aave v2 Ethereum for a [new one](https://etherscan.io/address/0xA4C2C730A4c01c64d54ce0165c27120989A3C743#code) with the following changes:
  - Base variable borrow: 0% -> **3%**
  - Variable borrow slope 1: 7% -> **14%**
  - Stable borrow slope 1: 10% -> **17%**

**[Polygon](https://polygonscan.com/address/0x3b6532efb7a60711f8f3fa77a589a726c836f4cf#code#F16#L16)**

First, replaces the current interest rate strategy of CRV on Aave v2 Polygon for a [new one](https://polygonscan.com/address/0xE4621DfD503A533f42bB5a45162eA3e5233Acd5F#code) with the following changes:
  - Base variable borrow: 0% -> **3%**
  - Variable borrow slope 1: 7% -> **14%**
  - Stable borrow slope 1: 10% -> **17%**

Second, replaces the current interest rate strategy of CRV on Aave v3 Polygon for a [new one](https://polygonscan.com/address/0xBefcd01681224555b74eAC87207eaF9Bc3361F59#code) with the following changes:
  - Base variable borrow: 0% -> **3%**
  - Variable borrow slope 1: 7% -> **14%**
  - Stable borrow slope 1: 0% -> **8%**
  - Stable borrow slope 2: 0% -> **300%**
  - Base Stable Rate Offset: 2% -> **3%**
  - Optimal point: 45% -> **70%**

Additionally, the proposal updates the supply cap of CRV on Aave v3 Polygon from 937'000 CRV to **1'125'240 CRV**, its borrow cap from 640'000 CRV to **900'190 CRV** and the Reserve Factor from 10% to **20%**.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: Payload encoded via multiple targets and calldatas, no delegatecall

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the procedure followed to submit the proposal.
