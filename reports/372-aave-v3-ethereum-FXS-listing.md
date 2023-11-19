# Proposal 372. Aave v3 Ethereum - listing of FXS

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=372](https://app.aave.com/governance/proposal/?proposalId=372)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-add-fxs-to-ethereum-v3/15112](https://governance.aave.com/t/arfc-add-fxs-to-ethereum-v3/15112)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists FXS (Frax Share) on the Aave v3 Ethereum pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x181af826496924baba20d0c7457033bf3e0f29b22c9873e42e727c6334ecfb6c](https://etherscan.io/tx/0x181af826496924baba20d0c7457033bf3e0f29b22c9873e42e727c6334ecfb6c)

```
- id: 372
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dabad81af85554e9ae636395611c58f7ec1aaec50000000000000000000000000000000000000000000000000000000000000012]
- withDelegatecalls: [false]
- startBlock: 18592893
- endBlock: 18612093
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xaf9ee1c1965d3483c0570f4d8a3e70744d08bc452e135331118169101af298c0
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/372.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/372.md)


**Payload report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/18.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/18.md)


<br>

### Technical analysis

The [proposal payload](https://etherscan.io/address/0x333d00b056a72787e4432fbcD075b32953677AEd#code#F32#L18) correctly uses the BGD's Aave Config Engine of Aave v3 Ethereum, in this case, its listing features.

We have verified this payload respects the interface required by the v3 config engine and effectively configures the FXS listing with the following initial parameters:

- The asset is enabled for borrowing and the interest rate strategy is configured the following way:
  - Base variable borrow: 0%
  - Variable borrow slope 1: 9%
  - Variable borrow slope 2: 300%
  - Optimal point: 45%

- The asset is enabled as collateral in isolation
- LTV: 35%
- Liquidation Threshold: 45%
- Liquidation Bonus: 10%
- Liquidation Protocol fee: 10%
- Reserve Factor: 20%
- Supply cap: 800'000 FXS
- Borrow cap: 500'000 FXS
- Debt ceiling: 4'000'000 USD
- No eMode category
- Flashlonable
- Not enabled for borrowing on isolation

The oracle used is a [Chainlink FXS/USD](https://etherscan.io/address/0x6Ebc52C8C1089be9eB3945C4350B68B8E4C2233f#readContract#F8).

The initial configuration is completely aligned with the [pre-approved by the community on Snapshot](https://snapshot.org/#/aave.eth/proposal/0xd8a8bdf3692666195895efbe0e885887c73b614273d6f0bd584c68afa9c11600)


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
