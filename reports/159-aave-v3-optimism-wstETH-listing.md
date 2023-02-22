# Proposal 159. Aave v3 Optimism - listing of wstETH

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=159](https://app.aave.com/governance/proposal/?proposalId=159)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-add-wsteth-to-aave-v3-on-optimism/10932](https://governance.aave.com/t/arc-add-wsteth-to-aave-v3-on-optimism/10932)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists wstETH (wrapped stETH) on the Aave v3 Optimism pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x9e1c2670a6fe4316a5fc149484b749f88619bff84ec269a9e2bb807d4c58ab63](https://etherscan.io/tx/0x9e1c2670a6fe4316a5fc149484b749f88619bff84ec269a9e2bb807d4c58ab63)

```
- id: 159
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x00000000000000000000000084893ee84e773e4a7a5738bd903dbe2a6e636b9e]
- withDelegatecalls: [true]
- startBlock: 16657440
- endBlock: 16676640
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xd9977b87efa9c8be6c30c4422ec588bc95133cbe1912310afcffaba67ba6010a
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/159.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/159.md)

**Optimism**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/159_optimism_5_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/159_optimism_5_0.md)

<br>

### Technical analysis

The [proposal payload](https://optimistic.etherscan.io/address/0x84893ee84e773e4a7a5738bd903dbe2a6e636b9e#code) follows the new approach for listings, using the [Aave V3 listing engine contract](https://optimistic.etherscan.io/address/0x7b8fa4540246554e77fcff140f9114de00f8bb8d#code), containing logic to expose a simple interface for listings, and do proper validations.

We have verified this payload respects the interface required by the v3 listing engine and effectively configures the wstETH listing with the following initial parameters:

- The asset is enabled for borrowing and the interest rate strategy follows the parameters on the forum:
  - Base variable borrow: 0.25%
  - Variable borrow slope 1: 4.5%
  - Variable borrow slope 2: 80%
  - Optimal point: 45%
- LTV: 70%
- Liquidation Threshold: 79%
- Liquidation Bonus: 7.2%
- Reserve Factor: 15%
- Liquidation protocol fee: 10%
- Supply cap: 6'000 wstETH
- Borrow cap: 940 wstETH
- No eMode category
- No isolation mode
- Flashloanable (Aave v3 Optimism doesn't have 3.0.1 yet, so all assets listed are flashloanable).
- Not enabled for borrowing on isolation

The oracle used is the [Chainlink WSTETH/USD feed](https://optimistic.etherscan.io/address/0x698B585CbC4407e2D54aa898B2600B53C68958f7#code).

The initial configuration is completely aligned with the description on the Aave governance forum.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
