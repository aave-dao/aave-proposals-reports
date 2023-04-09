# Proposal 197. Aave v3 Ethereum - listing of UNI, MKR, BAL and SNX

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=197](https://app.aave.com/governance/proposal/?proposalId=197)

<br>

### Governance forum discussions

[https://governance.aave.com/t/arfc-add-uni-to-ethereum-v3/11953](https://governance.aave.com/t/arfc-add-uni-to-ethereum-v3/11953)

[https://governance.aave.com/t/arfc-add-mkr-to-ethereum-v3/11954](https://governance.aave.com/t/arfc-add-mkr-to-ethereum-v3/11954)

[https://governance.aave.com/t/arfc-add-bal-ethereum-v3/11523](https://governance.aave.com/t/arfc-add-bal-ethereum-v3/11523)

[https://governance.aave.com/t/arfc-add-snx-to-ethereum-v3/11956](https://governance.aave.com/t/arfc-add-snx-to-ethereum-v3/11956)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists UNI, MKR, BAL and SNX on the Aave v3 Ethereum pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xa73ce803a14675968f12bfa680bf201d5b55ddea52835a7cb4246f6143f5959a](https://etherscan.io/tx/0xa73ce803a14675968f12bfa680bf201d5b55ddea52835a7cb4246f6143f5959a)

```
- id: 197
- creator: 0x62a43123fe71f9764f26554b3f5017627996816a
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xf146c735f39281d35fffee1a99e65b5307305a4f]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16983467
- endBlock: 17002667
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xd304f4b8429fe996ea4b8e1cb4aaa71a72e11992892c9a80b91158193c7da84d
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/197.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/197.md)


<br>

### Technical analysis

The [proposal payload](https://etherscan.io/address/0xf146c735f39281d35fffee1a99e65b5307305a4f#code#F23#L1) correctly uses the new [BGD's Aave Config Engine of Aave v3 Ethereum](https://etherscan.io/address/0xE202F2fc4b6A37Ba53cfD15bE42a762A645FCA07#code#F18#L1), in this case, its listing features.

We have verified the payload respects the interface required by the v3 config engine and lists the expected assets with the following configurations:

<br>

**UNI**

- The asset is enabled for borrowing and the interest rate strategy follows the parameters on Snapshot:
  - Base variable borrow: 0%
  - Variable borrow slope 1: 7%
  - Variable borrow slope 2: 300%
  - Optimal point: 45%
- The asset is enabled as collateral in isolation
- LTV: 65%
- Liquidation Threshold: 77%
- Liquidation Bonus: 10%
- Liquidation Protocol Fee: 10%
- Reserve Factor: 20%
- Supply cap: 2'000'000 UNI
- Borrow cap: 500'000 UNI
- Debt ceiling 17'000'000 USD
- No eMode category
- Flashlonable
- Not enabled for borrowing on isolation

**Similar as on Aave v2, aUNI is configured with a custom [DelegateAwareAToken](https://etherscan.io/address/0x21714092D90c7265F52fdfDae068EC11a23C6248#code) implementation, allowing for UNI voting power delegation of the underlying if the Aave governance would decide so.**

The oracle used is the [Chainlink UNI/USD feed](https://etherscan.io/address/0x553303d460EE0afB37EdFf9bE42922D8FF63220e#readContract#F4).

The initial configuration is completely aligned with [pre-approved Snapshot](https://snapshot.org/#/aave.eth/proposal/0x51d67ef69e901b34f1d111f2cd5d582c59cffa8d70b7939023febd20f7613b88).

<br>

**MKR**

- The asset is enabled for borrowing and the interest rate strategy follows the parameters on Snapshot:
  - Base variable borrow: 0%
  - Variable borrow slope 1: 7%
  - Variable borrow slope 2: 300%
  - Optimal point: 45%
- The asset is enabled as collateral in isolation
- LTV: 65%
- Liquidation Threshold: 70%
- Liquidation Bonus: 8.5%
- Liquidation Protocol Fee: 10%
- Reserve Factor: 20%
- Supply cap: 6'000 MKR
- Borrow cap: 1'500 MKR
- Debt ceiling 2'500'000 USD
- No eMode category
- Flashlonable
- Not enabled for borrowing on isolation

The oracle used is the [Chainlink MKR/USD feed](https://etherscan.io/address/0xec1D1B3b0443256cc3860e24a46F108e699484Aa#readContract#F4).

The initial configuration is completely aligned with [pre-approved Snapshot](https://snapshot.org/#/aave.eth/proposal/0xf4aec3fbab5096752be96f0e5b522f37318c1902cf8b897b049b7a94d478de73).

<br>

**BAL**

- The asset is enabled for borrowing and the interest rate strategy follows the parameters on the forum:
  - Base variable borrow: 3%
  - Variable borrow slope 1: 14%
  - Variable borrow slope 2: 150%
  - Optimal point: 80%
- The asset is enabled as collateral in isolation
- LTV: 57%
- Liquidation Threshold: 62%
- Liquidation Bonus: 8.3%
- Liquidation Protocol Fee: 10%
- Reserve Factor: 20%
- Supply cap: 700'000 BAL
- Borrow cap: 185'000 BAL
- Debt ceiling 2'900'000 USD
- No eMode category
- Flashlonable
- Not enabled for borrowing on isolation

The oracle used is the [Chainlink BAL/USD feed](https://etherscan.io/address/0xdF2917806E30300537aEB49A7663062F4d1F2b5F#readContract#F4).

The initial configuration is completely aligned with [pre-approved Snapshot](https://snapshot.org/#/aave.eth/proposal/0xe394799e4d006c15e0cb13155701de495888b7e7dad8f917a6b5dd1c8106cea5).

<br>

**SNX**

- The asset is enabled for borrowing and the interest rate strategy follows the parameters on the forum:
  - Base variable borrow: 3%
  - Variable borrow slope 1: 15%
  - Variable borrow slope 2: 100%
  - Optimal point: 80%
- The asset is enabled as collateral in isolation
- LTV: 49%
- Liquidation Threshold: 65%
- Liquidation Bonus: 8.5%
- Liquidation Protocol Fee: 10%
- Reserve Factor: 35%
- Supply cap: 2'000'000 SNX
- Borrow cap: 1'000'000 SNX
- Debt ceiling 2'500'000 USD
- No eMode category
- Flashlonable
- Not enabled for borrowing on isolation

The oracle used is the [Chainlink SNX/USD feed](https://etherscan.io/address/0xDC3EA94CD0AC27d9A86C180091e7f78C683d3699#readContract#F4).

The initial configuration is completely aligned with [pre-approved Snapshot](https://snapshot.org/#/aave.eth/proposal/0x5f232a89e10d67df3aad2907e8dce3bec9708596929b3254055cf37499969b89).


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
