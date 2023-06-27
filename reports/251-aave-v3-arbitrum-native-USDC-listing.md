# Proposal 251. Aave v3 Arbitrum - listing of native USDC

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=251](https://app.aave.com/governance/proposal/?proposalId=251)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-add-native-usdc-to-the-arbitrum-v3-pool/13568](https://governance.aave.com/t/arfc-add-native-usdc-to-the-arbitrum-v3-pool/13568)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists native USDC (USD Coin, issued directly on Arbitrum by Circle) on the Aave v3 Arbitrum pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x6aa542c91733c72ca516d5b7968ceaabf033b60c1bbf19bd38d46dc61340e591](https://etherscan.io/tx/0x6aa542c91733c72ca516d5b7968ceaabf033b60c1bbf19bd38d46dc61340e591)

```
- id: 251
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xd1b3e25fd7c8ae7caddc6f71b461b79cd4ddcfa3]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x0000000000000000000000007b20e2008c714f209131c7ec90294526e8f493cc]
- withDelegatecalls: [true]
- startBlock: 17536574
- endBlock: 17555774
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x1a8b44855daf7fa3af8cb5d83e8819856a745e29b24a0c143f153e017a7b1b13
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/251.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/251.md)

**Arbitrum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/251_Arbitrum_28.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/251_Arbitrum_28.md)


<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Arbitrum.

The [proposal payload](https://arbiscan.io/address/0x7b20e2008c714f209131c7ec90294526e8f493cc#code#F1#L15) correctly uses the BGD's Aave Config Engine of Aave v3 Arbitrum, in this case, its listing features.

We have verified this payload respects the interface required by the v3 config engine and effectively configures the USDC listing with the following initial parameters:

- The asset is enabled for borrowing and the interest rate strategy follows the parameters on the forum:
  - Base variable borrow: 0%
  - Variable borrow slope 1: 3.5%
  - Variable borrow slope 2: 60%
  - Optimal point: 90%

- The asset is enabled as collateral
- LTV: 81%
- Liquidation Threshold: 86%
- Liquidation Bonus: 5%
- Reserve Factor: 10%
- Liquidation Protocol Fee: 10%
- Supply cap: 41'000'000 USDCn
- Borrow cap: 41'000'000 USDCn
- e-mode category 1 (Stablecoins)
- No isolation mode
- Flashlonable
- Borrowable in isolation

The oracle used is the [Chainlink USDC/USD feed](https://arbiscan.io/address/0x50834F3163758fcC1Df9973b6e91f0F0F0434aD3#readContract#F8).

The initial configuration is completely aligned with the description on the Aave governance forum.

**Important** Even if this USDC is the native version of it, on the previous listing of the bridged USDC the symbol `USDC` has been used, so we agree with the decision to name within the protocol this new native version as `USDCn` to avoid name-clashing on tools build around the protocol.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
