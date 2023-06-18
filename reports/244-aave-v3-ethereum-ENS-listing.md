# Proposal 244. Aave v3 Ethereum - listing of ENS

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=244](https://app.aave.com/governance/proposal/?proposalId=244)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-add-ens-to-aave-v3-ethereum/13044](https://governance.aave.com/t/arfc-add-ens-to-aave-v3-ethereum/13044)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists ENS on the Aave v3 Ethereum pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xe39e12f9ee715b1b6908ed61519b1699d53604b3ad242d65ed1b7703b79149d8](https://etherscan.io/tx/0xe39e12f9ee715b1b6908ed61519b1699d53604b3ad242d65ed1b7703b79149d8)

```
- id: 244
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x4449a4d0c1ca7c0ea218f11c8a84dd9b8e633d43]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17485024
- endBlock: 17504224
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x767918bb5dba938c3d3cfa06c068a1179352749ac3d3735d9029061a38ffbb5a
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/244.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/244.md)


<br>

### Technical analysis

The [proposal payload](https://etherscan.io/address/0x4449a4d0c1ca7c0ea218f11c8a84dd9b8e633d43#code#F1#L15) correctly uses the BGD's Aave Config Engine of Aave v3 Ethereum, in this case, its listing features.

We have verified the payload respects the interface required by the v3 config engine and lists the ENS asset with the following configurations:

- The asset is enabled for borrowing and the interest rate strategy is configured as follows:
  - Base variable borrow: 0%
  - Variable borrow slope 1: 9%
  - Variable borrow slope 2: 300%
  - Optimal point: 45%
- The asset is enabled as collateral in isolation
- LTV: 39%
- Liquidation Threshold: 49%
- Liquidation Bonus: 8%
- Liquidation Protocol Fee: 10%
- Reserve Factor: 20%
- Supply cap: 1'000'000 ENS
- Borrow cap: 40'000 ENS
- Debt ceiling 3'900'000 USD
- No eMode category
- Flashlonable
- Not enabled for borrowing on isolation

The oracle used is the [Chainlink ENS/USD feed](https://etherscan.io/address/0x5C00128d4d1c2F4f652C267d7bcdD7aC99C16E16#readContract#F8)



<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
