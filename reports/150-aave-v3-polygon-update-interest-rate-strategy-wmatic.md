# Proposal 150. Aave v3 Polygon - update wMATIC interest rate strategies

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=150](https://app.aave.com/governance/proposal/?proposalId=150)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-aave-v3-polygon-wmatic-interest-rate-update/10290](https://governance.aave.com/t/arfc-aave-v3-polygon-wmatic-interest-rate-update/10290)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the interest rate strategy for wMATIC on the Aave v3 Polygon pool, and the supply and borrow caps of the asset.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x5ad415b37e54880d1a5c4ba0a84a94f5c43f311c612ea4899fc1a9204b3c999a](https://etherscan.io/tx/0x5ad415b37e54880d1a5c4ba0a84a94f5c43f311c612ea4899fc1a9204b3c999a)

```
- id: 150
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x0000000000000000000000007255791f9b2d44863c21ed1f484d444a74731ac6]
- withDelegatecalls: [true]
- startBlock: 16549267
- endBlock: 16568467
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x45876ec2905a472fed220dd1f12e0440770a16d521d78cb76f312032e33287ab
```

<br>

### Aave Seatbelt report

**Ethereum**
[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/150.md]([https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/150.md])



**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/150_fx_12_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/150_fx_12_0.md)

<br>

### Technical analysis

The proposal payload properly interacts with the Aave cross-chain governance system, via the the [CrosschainForwarderPolygon](https://etherscan.io/address/0x158a6bC04F0828318821baE797f50B0A1299d45b#code), to later execute the [proposal payload on Polygon](https://polygonscan.com/address/0x7255791f9b2d44863c21ed1f484d444a74731ac6#code) doing the following:

- Call `setReserveInterestRateStrategyAddress()` on the [Aave v3 Polygon Pool Configurator contract](https://polygonscan.com/address/0x8145eddDf43f50276641b55bd3AD95944510021E#code) to replace the interest rate strategy of wMATIC with the new proposed one.
- Call `setSupplyCap()` and `setBorrowCap()` also on the same Pool Configurator contract to set the supply cap to 47'000'000 wMATIC (from the current 32'880'000 wMATIC) and the borrow cap to 39'950'000 wMATIC (from the current 9'225'000 wMATIC).

In addition, we have verified the new rate strategy has the same parameters as those defined in the governance forum:

- Optimal point: 75%
- Base variable borrow rate: 0%
- Variable borrow slope 1: 6.1%
- Variable borrow slope 2: 100% 

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
