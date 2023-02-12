# Proposal 153. Aave v3 Ethereum - listing of rETH

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=153](https://app.aave.com/governance/proposal/?proposalId=153)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-onboard-reth-rocket-pool-eth-to-aave-v3-ethereum-market/11371](https://governance.aave.com/t/arc-onboard-reth-rocket-pool-eth-to-aave-v3-ethereum-market/11371)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists rETH (Rocket Pool ETH) on the Aave v3 Ethereum pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x366342a01fb6ec6b7f57202c1312eb11a998eb4b803771d15535501147e61785](https://etherscan.io/tx/0x366342a01fb6ec6b7f57202c1312eb11a998eb4b803771d15535501147e61785)

```
- id: 153
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x2dbbb5a1248bbbeddc2adee52a0995ed85f56006]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16593346
- endBlock: 16612546
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x3cbdcee6462df843a8ef50dc2130c02ac974ec884e09e60b36857278c98e310a
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/153.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/153.md)


<br>

### Technical analysis

The [proposal payload](https://etherscan.io/address/0x2dbbb5a1248bbbeddc2adee52a0995ed85f56006#code) follows the new approach for listings, using the [Aave V3 listing engine contract](https://etherscan.io/address/0xC51e6E38d406F98049622Ca54a6096a23826B426#code), containing logic to expose a simple interface for listings, and do proper validations.

We have verified this payload respects the interface required by the v3 listing engine and effectively configures the rETH listing with the following initial parameters:

- The asset is enabled for borrowing and the interest rate strategy follows the parameters on the forum:
  - Base variable borrow: 0
  - Variable borrow slope 1: 7%
  - Variable borrow slope 2: 300%
  - Optimal point: 45%
- LTV: 67%
- Liquidation Threshold: 74%
- Liquidation Bonus: 7.5%
- Reserve Factor: 15%
- Liquidation protocol fee: 10%
- Supply cap: 10'000 rETH
- Borrow cap: 1'200 rETH
- No eMode category
- No isolation mode
- Flashlonable
- Not enabled for borrowing on isolation

We have deployed [the oracle adapter](https://etherscan.io/address/0x05225Cd708bCa9253789C1374e4337a019e99D56#code) connected to the asset, and verified it works correctly. This adapter uses the ETH/USD Chainlink feed and the `exchangeRate()` of the rETH token, which given its update procedure, doesn't create any problem.

The initial configuration is completely aligned with the description on the Aave governance forum.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
