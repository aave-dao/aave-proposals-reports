# Proposal 112. Aave v2/v3 Polygon - Risk Parameter Updates 2022-10-21

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=112](https://app.aave.com/governance/proposal/?proposalId=112)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-price-manipulation-implications-on-aave-october-2022/10262](https://governance.aave.com/t/arc-price-manipulation-implications-on-aave-october-2022/10262)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

:link: :bridge_at_night: cross-chain execution

<br>

### Context

This proposal is a risk parameters update by Gauntlet, primarily setting supply and borrow caps in assets listed on Aave v2 and v3 Polygon.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xce32499bdc4f1c5707e20b29d33627717cebe7fe0fff1282ee93b227123801c9](https://etherscan.io/tx/0xce32499bdc4f1c5707e20b29d33627717cebe7fe0fff1282ee93b227123801c9)

```
- id: 112
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b,0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0,0]
- signatures: [execute(address),execute(address)]
- calldatas: [0x00000000000000000000000003232b5ee80369a88620615f8328beec1884b731,0x0000000000000000000000004393277b02ef3ca293990a772b7160a8c76f2443]
- withDelegatecalls: [true,true]
- startBlock: 15799327
- endBlock: 15818527
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x854fbd7bfa7e8d059e2b805396e4b92342b49612062ef5e214b170f396fd9cab
```

<br>

### Aave Seatbelt report


**Ethereum report:**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/112.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fhttps://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/112.md)

**Polygon reports:**

As the proposal affects Aave v2 and v3 Polygon, 2 different payloads will get executed. So there are 2 different Aave Seatbelt reports, one per payload.

*Aave v2 Polygon*

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/112_fx_5_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/112_fx_5_0.md)

*Aave v3 Polygon*

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/112_fx_5_1.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/112_fx_5_1.md)



<br>

### Technical analysis

Like on every Aave cross-chain proposal, this one follows the procedure defined on [https://github.com/bgd-labs/aave-v3-crosschain-listing-template](https://github.com/bgd-labs/aave-v3-crosschain-listing-template). This means that after execution on Ethereum, the proposal payload (2 in this case) will be queued on the Polygon side of the cross-chain infrastructure and, after 1 day of timelock there, will be open for execution.
Assuming that the cross-chain flow works properly, we have verified from a technical perspective that the payloads to be executed after timelock on Polygon do the following:


For Aave v2 Polygon:

1. Calls `configureReserveAsCollateral()` on the [Aave Pool Configurator](https://polygonscan.com/address/0x26db2b833021583566323e3b8985999981b9f1f3#code) for GHST, with the following changes:
    - Liquidation Threshold: **45% -> 40%**
    - **Disabling borrowing**
2. The payload also introduces a disabling of borrowing for DPI, but this has no effect on Aave v2 Polygon, as DPI is already disabled.


For Aave v3 Polygon:

By calling `setSupplyCap()` and `setBorrowCap()` on the [Pool Configurator](https://polygonscan.com/address/0x8145eddDf43f50276641b55bd3AD95944510021E#code), the following update of caps will be done:
1. AAVE:
  - Supply cap: **0 AAVE -> 36'820 AAVE**
2. BAL:
  - Supply cap: **0 BAL -> 284'600 BAL**
  - Borrow cap: **0 BAL -> 96'798 BAL**
3. CRV:
  - Supply cap: **0 CRV -> 937'700 CRV**
  - Borrow cap: **0 CRV -> 303'150 CRV**
4. DAI:
  - Borrow cap: **0 DAI -> 3'860'000 DAI**
5. DPI:
  - Supply cap: **0 DPI -> 1'417 DPI**
  - Borrow cap: **0 DPI -> 218 DPI**  
6. EUR:
  - Borrow cap: **0 EURS -> 728'520 EURS**
7. GHST:
  - Supply cap: **0 GHST -> 5'876'000 GHST**
  - Borrow cap: **0 GHST -> 904'000 GHST**
8. LINK:
  - Supply cap: **0 LINK -> 297'640 LINK**
  - Borrow cap: **0 LINK -> 51'029 LINK**
9. MAI:
  - Borrow cap: **0 MAI -> 359'980 MAI**
10. WMATIC:
  - Supply cap: **0 WMATIC -> 32'880'000 WMATIC**
  - Borrow cap: **0 WMATIC -> 9'225'000 WMATIC**
11. SUSHI:
  - Supply cap: **0 SUSHI -> 299'320 SUSHI**
  - Borrow cap: **0 SUSHI -> 102'484 SUSHI**
12. USDC:
  - Borrow cap: **0 USDC -> 30'680'000 USDC**
13. USDT:
  - Borrow cap: **0 USDT -> 5'060'000 USDT**
14. WBTC:
  - Supply cap: **0 WBTC -> 1'548 WBTC**
  - Borrow cap: **0 WBTC -> 155 WBTC**
15. WETH:
  - Supply cap: **0 WETH -> 26'900 WETH**
  - Borrow cap: **0 WETH -> 2'690 WETH**


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

:white_check_mark: With BGD writing the payload, at least another party reviewed it.
