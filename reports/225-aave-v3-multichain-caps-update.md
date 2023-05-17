# Proposal 225. Aave v3 Polygon, Arbitrum - Caps update

<br>


### Voting link

[https://app.aave.com/governance/proposal/?proposalId=225](https://app.aave.com/governance/proposal/?proposalId=225)

<br>

### Governance forum discussions

[https://governance.aave.com/t/arfc-increase-wsteth-supply-cap-on-polygon-v3/12971/2](https://governance.aave.com/t/arfc-increase-wsteth-supply-cap-on-polygon-v3/12971/2)

[https://governance.aave.com/t/arfc-increase-stmatic-supplycap/12998](https://governance.aave.com/t/arfc-increase-stmatic-supplycap/12998)

[https://governance.aave.com/t/arfc-wsteth-supply-cap-increase-arbitrum-v3/13016/4](https://governance.aave.com/t/arfc-wsteth-supply-cap-increase-arbitrum-v3/13016/4)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates supply and borrow caps of multiple assets across Aave v3 Polygon and Arbitrum.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xe790b0697fc4554e369a5981471b0b9c7d0c94e3bc17dec738b4f950d6f600fb](https://etherscan.io/tx/0xe790b0697fc4554e369a5981471b0b9c7d0c94e3bc17dec738b4f950d6f600fb)

```
- id: 225
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b,0xd1b3e25fd7c8ae7caddc6f71b461b79cd4ddcfa3]
- values: [0,0]
- signatures: [execute(address),execute(address)]
- calldatas: [0x000000000000000000000000a4c2c730a4c01c64d54ce0165c27120989a3c743,0x00000000000000000000000052d5f9f884ca21c27e2100735d793c6771eab793]
- withDelegatecalls: [true,true]
- startBlock: 17252212
- endBlock: 17271412
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xedac26e6134bbb7124820d59ae30673245ed5f62d5ecfb32083a8f8a284b52de
```

<br>

### Aave Seatbelt reports

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/225.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/225.md)


**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/225_fx_38_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/225_fx_38_0.md)

**Arbitrum**

Aave Seatbelt doesn't support Arbitrum yet.


<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system in the parts communicating with Polygon and Arbitrum.

Regarding each payload, the changes applied are the following:

**[Polygon](https://polygonscan.com/address/0xa4c2c730a4c01c64d54ce0165c27120989a3c743#code#F23#L1)**

- wstETH:
  - Supply cap: 1'800 wstETH -> **2'400 wstETH**

- stMATIC:
  - Supply cap: 25'000'000 stMATIC -> **30'000'000 stMATIC**

**[Arbitrum](https://arbiscan.io/address/0x52d5f9f884ca21c27e2100735d793c6771eab793#code#F23#L1)**

- wstETH:
  - Supply cap: 4'650 wstETH -> **9'300 wstETH** 


<br>

The caps updates are aligned with those defined in the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
