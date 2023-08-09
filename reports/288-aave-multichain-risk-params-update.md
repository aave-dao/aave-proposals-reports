# Proposal 288. Aave v3 Ethereum, Polygon - Risk parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=288](https://app.aave.com/governance/proposal/?proposalId=288)

<br>

### Governance forum discussion

[https://governance.aave.com/t/gauntlet-recommendation-to-lower-crv-lt-on-v3-ethereum-and-polygon/14302](https://governance.aave.com/t/gauntlet-recommendation-to-lower-crv-lt-on-v3-ethereum-and-polygon/14302)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal adjusts different risk parameters of CRV on both Aave v3 Ethereum and Aave v3 Polygon.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xbb2e4cbc4025c96a920335b2d8d74ac5fee7b40aeb31065d907c123017a6c255](https://etherscan.io/tx/0xbb2e4cbc4025c96a920335b2d8d74ac5fee7b40aeb31065d907c123017a6c255)

```
- id: 288
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x7aa759a57c6b039a93e93683facd14209ee9a3dd,0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0,0]
- signatures: [execute(),execute(address)]
- calldatas: [0x,0x000000000000000000000000c12ad8b3d242b1eddc1c8319d1d58608e67043ed]
- withDelegatecalls: [true,true]
- startBlock: 17851744
- endBlock: 17870944
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x4940eb2481c308072d4e2431c167477918e48edf25551c54bdac13d1f78d8497
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/288.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/288.md)


**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/288_Polygon_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/288_Polygon_pending_0.md)

<br>

### Technical analysis

We have verified the proposal properly uses cross-chain governance (for the Polygon payload), and the BGD Aave Config Engine (v3 Ethereum and Polygon) to do the following changes on 2 separate payloads:

[Aave v3 Ethereum](https://etherscan.io/address/0x7aa759a57c6b039a93e93683facd14209ee9a3dd#code)

CRV
- LTV: 55% -> **35%**
- Liquidation Threshold: 61% -> **41%**
- Debt ceiling: 20'900'000 USD -> **5'000'000 USD**

<br>

[Aave v3 Polygon](https://polygonscan.com/address/0xc12ad8b3d242b1eddc1c8319d1d58608e67043ed#code#F1#L14)

CRV
- LTV: 70% -> **35%**
- Liquidation Threshold: 75% -> **65%**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:x: BGD reviewed the procedure followed to submit the proposal.
