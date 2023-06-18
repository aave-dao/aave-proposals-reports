# Proposal 245. Aave v3 Ethereum - listing of 1INCH

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=245](https://app.aave.com/governance/proposal/?proposalId=245)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-add-1inch-to-aave-v3-ethereum/13043](https://governance.aave.com/t/arfc-add-1inch-to-aave-v3-ethereum/13043)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists 1INCH on the Aave v3 Ethereum pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x22baa2f8472c99b861820ee45ba19f587acce1da16448f7b83b921eb66fbe4d9](https://etherscan.io/tx/0x22baa2f8472c99b861820ee45ba19f587acce1da16448f7b83b921eb66fbe4d9)

```
- id: 245
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x134c50556de1a83dd947c9460a58d8d60a289cea]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17485046
- endBlock: 17504246
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x111f8f9fddd053337e3251dad1a74474c42dba045a55aed0f38db8099ca84778
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/245.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/245.md)


<br>

### Technical analysis

The [proposal payload](https://etherscan.io/address/0x134c50556de1a83dd947c9460a58d8d60a289cea#code#F1#L15) correctly uses the BGD's Aave Config Engine of Aave v3 Ethereum, in this case, its listing features.

We have verified the payload respects the interface required by the v3 config engine and lists the 1INCH asset with the following configurations:

- The asset is enabled for borrowing and the interest rate strategy is configured as follows:
  - Base variable borrow: 0%
  - Variable borrow slope 1: 9%
  - Variable borrow slope 2: 300%
  - Optimal point: 45%
- The asset is enabled as collateral in isolation
- LTV: 57%
- Liquidation Threshold: 67%
- Liquidation Bonus: 7.50%
- Liquidation Protocol Fee: 10%
- Reserve Factor: 20%
- Supply cap: 22'000'000 1INCH
- Borrow cap: 720'000 1INCH
- Debt ceiling 4'500'000 USD
- No eMode category
- Flashlonable
- Not enabled for borrowing on isolation

The oracle used is the [Chainlink 1INCH/USD feed](https://etherscan.io/address/0xc929ad75B72593967DE83E7F7Cda0493458261D9#readContract#F8)



<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
