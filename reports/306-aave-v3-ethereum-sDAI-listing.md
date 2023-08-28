# Proposal 306. Aave v3 Ethereum - listing of sDAI and DAI, WETH parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=306](https://app.aave.com/governance/proposal/?proposalId=306)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-sdai-aave-v3-onboarding/14410](https://governance.aave.com/t/arfc-sdai-aave-v3-onboarding/14410)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

:wrench: :bar_chart: params-update

<br>

### Context

This proposal lists sDAI on the Aave v3 Ethereum pool and changes different parameters on the DAI asset, also on v2 Ethereum.

Additionally, the proposal adjusts the optimal usage point of WETH on Aave v3 Ethereum.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x2f11e827a98cdfdc6c8dc9924f5e1d6133ac693620cc45a4af6f9c9f9c851ac2](https://etherscan.io/tx/0x2f11e827a98cdfdc6c8dc9924f5e1d6133ac693620cc45a4af6f9c9f9c851ac2)

```
- id: 306
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x5bfb45198ed029443f0d41ca6ed70789ddd9fd01,0xf2a9129773542686ffa009f29f3aa02ae1c0edf7]
- values: [0,0]
- signatures: [execute(),execute()]
- calldatas: [0x,0x]
- withDelegatecalls: [true,true]
- startBlock: 17987192
- endBlock: 18006392
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x43564b8533a1941a0ded6928eb7606f46c11b9ee65f5f88141ff3ba51c3ae78f
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/306.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/306.md)


<br>

### Technical analysis

The proposal is composed of 2 payloads: one for Aave v3 Ethereum, the other for Aave v2 Ethereum.

<br>

---

<br>

[Aave v3 Ethereum payload](https://etherscan.io/address/0x5bfb45198ed029443f0d41ca6ed70789ddd9fd01#code#F1#L14)

This payload does the following:

1. Listing of sDAI

    We have verified this payload respects the interface required by the v3 config engine and effectively configures the sDAI listing with the following initial parameters:

    - The asset is not enabled for borrowing.
    - The asset is enabled as collateral.
    - LTV: 77%
    - Liquidation Threshold: 80%
    - Liquidation Bonus: 4.5%
    - Liquidation Protocol fee: 10%
    - Reserve Factor: 20%
    - Supply cap: 340'000'000 sDAI
    - Borrow cap: 0 sDAI
    - No eMode category
    - Flashlonable
    - Not enabled for borrowing on isolation

    The oracle used is a [BGD CL Synchronicity Price Adapter](https://etherscan.io/address/0x29081f7aB5a644716EfcDC10D5c926c5fEe9F72B#code) using the [DAI/USD CL price feed](https://etherscan.io/address/0xAed0c38402a5d19df6E4c03F4E2DceD6e29c1ee9#readContract#F8) and the sDAI/DAI exchange rate from the [MakerDAO Pot smart contract](https://etherscan.io/address/0x197E90f9FAD81970bA7976f33CbD77088E5D7cf7#code).

    The initial configuration is aligned with the [pre-approved by the community on Snapshot](https://snapshot.org/#/aave.eth/proposal/0xb41600e3f74bfa520549106fee4d21e7f674c5a79fbf1f7ca16947563474a4d7).

  <br>

  2. Interest rate strategy update of DAI
    
      The changes are the following:
        - Variable borrow slope 1: 4% -> **5%**
        - Base stable borrow rate: 5% -> **6%**
        - Optimal point: 80% -> **90%**

  <br>

  3. Interest rate strategy update on WETH

      - Base variable borrow: 1% -> **0%**
      - Optimal point: 80% -> **90%**

<br>

  4. Update DAI Reserve Factor (RF)

      **The proposal intended to update the Reserve Factor of DAI from 10% to 20%, but due to an interface incompatibility on the payload, this change will not take effect**

<br>

---

<br>

[Aave v2 Ethereum payload](https://etherscan.io/address/0xf2a9129773542686ffa009f29f3aa02ae1c0edf7#code#F1#L13)

This payload does the following:

  1. Interest rate strategy update of DAI

      The changes are the following:
        - Variable borrow slope 1: 4% -> **5%**

  <br>

  2. Disable stable rate mode for DAI

  <br>

  3. Update DAI Reserve Factor (RF)
    - Reserve factor: 15% -> **25%**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
