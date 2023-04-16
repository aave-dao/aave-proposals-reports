# Proposal 201. Aave v3 Ethereum - listing of LDO

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=201](https://app.aave.com/governance/proposal/?proposalId=201)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-add-support-for-ldo-on-ethereum-v3/12045](https://governance.aave.com/t/arfc-add-support-for-ldo-on-ethereum-v3/12045)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists LDO on the Aave v3 Ethereum pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xa4ef4446220f8b1c78e248ae3f932312eb1e888af8e55b697a027145b6c2c20b](https://etherscan.io/tx/0xa4ef4446220f8b1c78e248ae3f932312eb1e888af8e55b697a027145b6c2c20b)

```
- id: 201
- creator: 0x62a43123fe71f9764f26554b3f5017627996816a
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x7b766a02eba6d8651eeebdeb886323fc64bf1739]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17039685
- endBlock: 17058885
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x15c80b04cf6ba566a61b13f4a403bda6d13ecdd1cd5aec5ae50841a582050105
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/201.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/201.md)


<br>

### Technical analysis

The [proposal payload](https://etherscan.io/address/0x7b766a02eba6d8651eeebdeb886323fc64bf1739#code#F21#L17) correctly uses the new [BGD's Aave Config Engine of Aave v3 Ethereum](https://etherscan.io/address/0xE202F2fc4b6A37Ba53cfD15bE42a762A645FCA07#code#F18#L1), in this case, its listing features.

We have verified the payload respects the interface required by the v3 config engine and lists the LDO asset with the following configurations:

<br>

**LDO**

- The asset is enabled for borrowing and the interest rate strategy follows the parameters on Snapshot:
  - Base variable borrow: 0%
  - Variable borrow slope 1: 7%
  - Variable borrow slope 2: 300%
  - Optimal point: 45%
- The asset is enabled as collateral in isolation
- LTV: 40%
- Liquidation Threshold: 50%
- Liquidation Bonus: 9%
- Liquidation Protocol Fee: 10%
- Reserve Factor: 20%
- Supply cap: 6'000'000 LDO
- Borrow cap: 3'000'000 LDO
- Debt ceiling 7'500'000 USD
- No eMode category
- Flashlonable
- Not enabled for borrowing on isolation

The oracle used is a BGD CL Synchronicity Price Adapter using the underlying LDO/ETH and ETH/USD, with a resulting [LDO/USD](https://etherscan.io/address/0xb01e6C9af83879B8e06a092f0DD94309c0D497E4#readContract#F6)

The initial configuration is completely aligned with [pre-approved Snapshot](https://snapshot.org/#/aave.eth/proposal/0x953f0edc544fe50e68a0aa19d31542d15458bc3394478a31a294f748198fa906).


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
