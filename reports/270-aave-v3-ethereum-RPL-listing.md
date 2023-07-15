# Proposal 270. Aave v3 Ethereum - listing of RPL

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=270](https://app.aave.com/governance/proposal/?proposalId=270)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-add-rpl-to-ethereum-v3/13181](https://governance.aave.com/t/arfc-add-rpl-to-ethereum-v3/13181)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists RPL on the Aave v3 Ethereum pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xe253a9c712f14a54410781040af4da7b7e85e0bcba3755162645a4fd79162416](https://etherscan.io/tx/0xe253a9c712f14a54410781040af4da7b7e85e0bcba3755162645a4fd79162416)

```
- id: 270
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x5a95c30ff6dfeecf264459c342bc01888867e3e8]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17678310
- endBlock: 17697510
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xccb773a1223c8f50ddad3097656eab771fc5a73fe6d7bad297d093c34c2df7b2
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/270.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/270.md)


<br>

### Technical analysis

The [proposal payload](https://etherscan.io/address/0x5a95c30ff6dfeecf264459c342bc01888867e3e8#code#F1#L12) correctly uses the BGD's Aave Config Engine of Aave v3 Ethereum, in this case, its listing features.

We have verified this payload respects the interface required by the v3 config engine and effectively configures the RPL listing with the following initial parameters:

- The asset is enabled for borrowing and the interest rate strategy is configured the following way:
  - Base variable borrow: 0%
  - Variable borrow slope 1: 8.5%
  - Variable borrow slope 2: 87%
  - Optimal point: 80%

- The asset is NOT enabled as collateral
- Reserve Factor: 20%
- Supply cap: 105'000 RPL
- Borrow cap: 105'000 RPL
- No eMode category
- Flashlonable
- Not enabled for borrowing on isolation

The oracle used is a [Chainlink RPL/USD](https://etherscan.io/address/0x4E155eD98aFE9034b7A5962f6C84c86d869daA9d#readContract#F8).

The initial configuration is completely aligned with the [pre-approved by the community on Snapshot](https://snapshot.org/#/aave.eth/proposal/0x036f9ce8b4a9fef0156ccf6b2a205d56d4f23b7ab9a485a16d7c8173cd85a316)


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
