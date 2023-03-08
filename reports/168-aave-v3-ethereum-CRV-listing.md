# Proposal 168. Aave v3 Ethereum - listing of CRV

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=168](https://app.aave.com/governance/proposal/?proposalId=168)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-add-crv-to-ethereum-v3/11532](https://governance.aave.com/t/arfc-add-crv-to-ethereum-v3/11532)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists CRV (Curve DAO Token) on the Aave v3 Ethereum pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x51e49e6ada15234d34b3c627f8b8b2bc06ae9f71207bde2173a1a47f2fd56633](https://etherscan.io/tx/0x51e49e6ada15234d34b3c627f8b8b2bc06ae9f71207bde2173a1a47f2fd56633)

```
- id: 168
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x5594475f068f814bdeb2d21b1676431a376322f5]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16755627
- endBlock: 16774827
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x5facc2129293778f8b9f474ee578d3368adc34a0bb4a1ba5e3f2e0b3b3f1a50b
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/168.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/168.md)


<br>

### Technical analysis

The [proposal payload](https://etherscan.io/address/0x5594475f068f814bdeb2d21b1676431a376322f5#code#F20#L1) follows the new approach for listings, using the [Aave V3 listing engine contract](https://etherscan.io/address/0xC51e6E38d406F98049622Ca54a6096a23826B426#code), containing logic to expose a simple interface for listings, and do proper validations.

We have verified this payload respects the interface required by the v3 listing engine and effectively configures the CRV listing with the following initial parameters:

- The asset is enabled for borrowing and the interest rate strategy follows the parameters on the forum:
  - Base variable borrow: 3%
  - Variable borrow slope 1: 14%
  - Variable borrow slope 2: 300%
  - Optimal point: 70%
- The asset is enabled as collateral in isolation
- LTV: 55%
- Liquidation Threshold: 61%
- Liquidation Bonus: 8.3%
- Debt ceiling: 20'900'000 USD
- Reserve Factor: 20%
- Liquidation protocol fee: 10%
- Supply cap: 62'500'000 CRV
- Borrow cap: 7'700'000 CRV
- No eMode category
- Flashlonable
- Not enabled for borrowing on isolation

The oracle used is the [Chainlink CRV/USD feed](https://etherscan.io/address/0xCd627aA160A6fA45Eb793D19Ef54f5062F20f33f#code).

The initial configuration is completely aligned with the description on the Aave governance forum.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
