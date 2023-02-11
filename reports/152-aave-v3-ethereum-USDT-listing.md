# Proposal 152. Aave v3 Ethereum - listing of USDT

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=152](https://app.aave.com/governance/proposal/?proposalId=152)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-add-usdt-to-ethereum-v3-market/11536](https://governance.aave.com/t/arfc-add-usdt-to-ethereum-v3-market/11536)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists USDT (Tether USD) on the Aave v3 Ethereum pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x54aff69f2bb3e6583349e6d4212858a155e5f114caf4b214551712b87dd5529a](https://etherscan.io/tx/0x54aff69f2bb3e6583349e6d4212858a155e5f114caf4b214551712b87dd5529a)

```
- id: 152
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x3b45bbc2b69fafab95fd91b10f39ccb5dd92facb]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16591104
- endBlock: 16610304
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x808868979965100b100d66218d024cb4a3dbde566bd6f4f0530141f42cf97f74
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/152.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/152.md)


<br>

### Technical analysis

The [proposal payload](https://etherscan.io/address/0x3b45bbc2b69fafab95fd91b10f39ccb5dd92facb#code) follows the new approach for listings, using the [Aave V3 listing engine contract](https://etherscan.io/address/0xC51e6E38d406F98049622Ca54a6096a23826B426#code), containing logic to expose a simple interface for listings, and do proper validations.

We have verified this payload respects the interface required by the v3 listing engine and effectively configures the USDT listing with the following initial parameters:

- The asset is enabled for borrowing and the interest rate strategy follows the parameters on the forum:
  - Base variable borrow: 0
  - Variable borrow slope 1: 4%
  - Variable borrow slope 2: 72%
  - Optimal point: 90%
- The asset is not enabled as collateral
- Reserve Factor: 10%
- Liquidation protocol fee: 10%
- Supply cap: 200'000'000 USDT
- Borrow cap: 185'000'000 USDT
- No eMode category
- No isolation mode
- Flashlonable
- Not enabled for borrowing on isolation

The oracle used is the [Chainlink USDT/USD feed](https://etherscan.io/address/0x3E7d1eAB13ad0104d2750B8863b489D65364e32D#code).

The initial configuration is completely aligned with the description on the Aave governance forum.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
