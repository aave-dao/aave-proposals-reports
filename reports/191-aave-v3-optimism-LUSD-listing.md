# Proposal 191. Aave v3 Optimism - listing of LUSD

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=191](https://app.aave.com/governance/proposal/?proposalId=191)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-add-lusd-to-optimism-v3-market/12113](https://governance.aave.com/t/arfc-add-lusd-to-optimism-v3-market/12113)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists LUSD (LUSD Stablecoin, Liquity) on the Aave v3 Optimism pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x4c3d4bebfec54b95994ac7555cdec5fa8cacba4800a22d776d089a9550f958c9](https://etherscan.io/tx/0x4c3d4bebfec54b95994ac7555cdec5fa8cacba4800a22d776d089a9550f958c9)

```
- id: 191
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000f585f8cf39c1ef5353326e0352b9e237f9a52587]
- withDelegatecalls: [true]
- startBlock: 16939593
- endBlock: 16958793
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xfa17ef2b6d70703ca5f2919932559937352590b637cc8f1425bd6615311079a7
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/191.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/191.md)


<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Optimism.

The [proposal payload](https://optimistic.etherscan.io/address/0xf585f8cf39c1ef5353326e0352b9e237f9a52587#code#F21#L1) correctly uses the new [BGD's Aave Config Engine of Aave v3 Optimism](https://optimistic.etherscan.io/address/0x7a9a9c14b35e58ffa1cc84ab421ace0fdcd289e3#code#F18#L1), in this case, its listing features.

We have verified this payload respects the interface required by the v3 config engine and effectively configures the LUSD listing with the following initial parameters:

- The asset is enabled for borrowing and the interest rate strategy follows the parameters on the forum:
  - Base variable borrow: 0%
  - Variable borrow slope 1: 4%
  - Variable borrow slope 2: 87%
  - Optimal point: 80%

- The asset is not enabled as collateral
- Reserve Factor: 10%
- Supply cap: 3'000'000 LUSD
- Borrow cap: 1'210'000 LUSD
- No eMode category
- No isolation mode
- Not flashlonable
- Not enabled for borrowing on isolation

The oracle used is the [Chainlink LUSD/USD feed](https://optimistic.etherscan.io/address/0x9dfc79Aaeb5bb0f96C6e9402671981CdFc424052#code).

The initial configuration is completely aligned with the description on the Aave governance forum.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
