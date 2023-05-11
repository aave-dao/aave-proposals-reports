# Proposal 219. Aave v3 Arbitrum - listing of MAI

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=219](https://app.aave.com/governance/proposal/?proposalId=219)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-add-mai-to-arbitrum-aave-v3-market/12759](https://governance.aave.com/t/arfc-add-mai-to-arbitrum-aave-v3-market/12759)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists MAI on the Aave v3 Arbitrum pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x7cc7d8963a7a9047534a21cc0902223ccd404881ed708c6935771a22509756f0](https://etherscan.io/tx/0x7cc7d8963a7a9047534a21cc0902223ccd404881ed708c6935771a22509756f0)

```
- id: 219
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xd1b3e25fd7c8ae7caddc6f71b461b79cd4ddcfa3]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x00000000000000000000000089f1e458b51749ed887c382f06459fc8d7ff7846]
- withDelegatecalls: [true]
- startBlock: 17223452
- endBlock: 17242652
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x18739980bfc9374ed44c05152e5b47b12b33883fe2a6ad3e13e70cec9132f372
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/219.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/219.md)

**Arbitrum**

Aave Seatbelt doesn't support Arbitrum yet.


<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Arbitrum.

The [proposal payload](https://arbiscan.io/address/0x89f1e458b51749ed887c382f06459fc8d7ff7846#code#F22#L15) correctly uses the [BGD's Aave Config Engine of Aave v3 Arbitrum](https://arbiscan.io/address/0x0efdfc1a940de4e7e6acc9bb801481f81b17fd20#code#F18#L1), in this case, its listing features.

We have verified the payload respects the interface required by the v3 config engine and lists the MAI asset with the following configurations:

<br>

**MAI**

- The asset is enabled for borrowing and the interest rate strategy follows the parameters on Snapshot:
  - Base variable borrow: 0%
  - Variable borrow slope 1: 4%
  - Variable borrow slope 2: 75%
  - Optimal point: 80%
- The asset is enabled as collateral in isolation
- LTV: 75%
- Liquidation Threshold: 80%
- Liquidation Bonus: 5%
- Liquidation Protocol Fee: 10%
- Reserve Factor: 20%
- Supply cap: 4'800'000 MAI
- Borrow cap: 2'400'000 MAI
- Debt ceiling 1'200'000 USD
- No eMode category
- Not flashlonable
- Not enabled for borrowing on isolation

The oracle used is a [Chainlink MAI/USD feed](https://arbiscan.io/address/0x59644ec622243878d1464A9504F9e9a31294128a#readContract#F8).

The initial configuration is completely aligned with the [recommendations of risk providers in the Aave governance forum](https://governance.aave.com/t/arfc-add-mai-to-arbitrum-aave-v3-market/12759/5).


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
