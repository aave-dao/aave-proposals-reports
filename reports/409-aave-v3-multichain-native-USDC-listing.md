# Proposal 409. Aave v3 Polygon, Base, Optimism, Arbitrum - listing of native USDC and params update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=409](https://app.aave.com/governance/proposal/?proposalId=409)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-onboard-native-usdc-to-aave-v3-markets/15720](https://governance.aave.com/t/arfc-onboard-native-usdc-to-aave-v3-markets/15720)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

:wrench: :bar_chart: params-update

<br>

### Context

This proposal lists native USDC (USDC coin) on the Aave v3 Polygon and Base. Additionally, it also updates certain configurations (RF, caps) for "bridged" and "native" USDC on Aave v3 Optimism and Arbitrum.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x5d758fff34938152dc43f586b54471c9e9bc91a015fbfc5a460e478c50483643](https://etherscan.io/tx/0x5d758fff34938152dc43f586b54471c9e9bc91a015fbfc5a460e478c50483643)

```
- id: 409
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7,0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7,0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7,0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0,0,0,0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40)),forwardPayloadForExecution((uint256,uint8,address,uint40)),forwardPayloadForExecution((uint256,uint8,address,uint40)),forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000890000000000000000000000000000000000000000000000000000000000000001000000000000000000000000401b5d0294e23637c18fcc38b1bca814cda2637c0000000000000000000000000000000000000000000000000000000000000017,0x000000000000000000000000000000000000000000000000000000000000000a00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000e1a3af1f9cc76a62ed31ededca291e63632e7c40000000000000000000000000000000000000000000000000000000000000007,0x000000000000000000000000000000000000000000000000000000000000a4b1000000000000000000000000000000000000000000000000000000000000000100000000000000000000000089644ca1bb8064760312ae4f03ea41b05da3637c0000000000000000000000000000000000000000000000000000000000000006,0x000000000000000000000000000000000000000000000000000000000000210500000000000000000000000000000000000000000000000000000000000000010000000000000000000000002dc219e716793fb4b21548c0f009ba3af753ab010000000000000000000000000000000000000000000000000000000000000004]
- withDelegatecalls: [false,false,false,false]
- startBlock: 18797527
- endBlock: 18816727
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x201c7d09c8b5cf06ff06e8011b8e3459e05f2083b05bbc046614604c5acd02d3
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/409.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/409.md)


**Payloads reports**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/23.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/23.md)

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/7.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/7.md)

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/6.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/6.md)

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/4.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/4.md)


<br>

### Technical analysis

This proposal contains 4 different payload, one per network affected.


[Polygon payload](https://polygonscan.com/address/0x2D8318a89Fe951a3Cf80cDc7e836246E011F417C#code#F1#L18)

The proposal payload correctly uses the BGD's Aave Config Engine of Aave v3 Polygon, in this case, its listing features.

We have verified this payload respects the interface required by the v3 config engine and effectively configures the native USDCn (native) listing with the following initial parameters:

- The asset is enabled for borrowing and the interest rate strategy is configured the following way:
  - Base variable borrow: 0%
  - Variable borrow slope 1: 5%
  - Variable borrow slope 2: 60%
  - Optimal point: 90%

- The asset is enabled as collateral
- LTV: 77%
- Liquidation Threshold: 80%
- Liquidation Bonus: 5%
- Liquidation Protocol fee: 10%
- Reserve Factor: 10%
- Supply cap: 50'000'000 USDCn
- Borrow cap: 45'000'000 USDCn
- Stablecoins eMode category
- Flashlonable
- Disabled for borrowing on isolation

The oracle used is a [Chainlink USDC/USD](https://polygonscan.com/address/0xfE4A8cc5b5B2366C1B58Bea3858e81843581b2F7#readContract#F8).

<br>

---

<br>

Additionally, the following changes are applied to USDC (non-native):

- Supply cap: 150'000'000 USDC -> **40'000'000 USDC**
- Borrow cap: 100'000'000 USDC -> **36'000'000 USDC**
- Reserve factor: 10% -> **20%**
- Variable slope 1: 5% -> **7%**
- Variable slope 2: 60% -> **80%**
- LTV: 82.5% -> **77%**
- Liquidation Threshold: 85% -> **80%**
- Liquidation bonus: 4% -> **5%**
- Reserve factor: 10% -> **20%** 

<br>

<br>

[Base payload](https://basescan.org/address/0xCAB466a6bEd466316B20151c9526aFC7654d00F2#code#F1#L18)

The proposal payload correctly uses the BGD's Aave Config Engine of Aave v3 Base, in this case, its listing features.

We have verified this payload respects the interface required by the v3 config engine and effectively configures the native USDC (native) listing with the following initial parameters:

- The asset is enabled for borrowing and the interest rate strategy is configured the following way:
  - Base variable borrow: 0%
  - Variable borrow slope 1: 5%
  - Variable borrow slope 2: 60%
  - Optimal point: 90%

- The asset is enabled as collateral
- LTV: 77%
- Liquidation Threshold: 80%
- Liquidation Bonus: 5%
- Liquidation Protocol fee: 10%
- Reserve Factor: 10%
- Supply cap: 10'000'000 USDC
- Borrow cap: 9'000'000 USDC
- No eMode category
- Flashlonable
- Disabled for borrowing on isolation

The oracle used is a [Chainlink USDC/USD](https://basescan.org/address/0x7e860098F58bBFC8648a4311b374B1D669a2bc6B#readContract#F8).

<br>

---

<br>

Additionally, the following changes are applied to USDbC (non-native):

- Supply cap: 8'000'000 USDbC -> **2'000'000 USDbC**
- Borrow cap: 6'500'000 USDC -> **2'000'000 USDbC**
- Reserve factor: 10% -> **20%**
- Variable slope 1: 5% -> **7%**
- Variable slope 2: 60% -> **80%**
- Reserve factor: 10% -> **20%**


<br>

<br>

[Optimism payload](https://optimistic.etherscan.io/address/0xCAB466a6bEd466316B20151c9526aFC7654d00F2#code#F1#L18)

We have verified this payload respects the interface required by the v3 config engine to do the following parameters changes:

USDC

- Variable slope 1: 5% -> **7%**
- LTV: 80% -> **77%**
- Liquidation Threshold: 85% -> **80%**


<br>

USDC.e

- Supply cap: 25'000'000 USDC.e -> **18'000'000 USDC.e**
- Borrow cap: 20'000'000 USDC.e -> **15'500'000 USDC.e**
- Variable slope 1: 5% -> **7%**
- Variable slope 2: 60% -> **80%**

<br>

<br>


[Arbitrum payload](https://arbiscan.io/address/0x92B4631F688C37de8cAb93652a96a92475A7F412#code#F1#L18)

We have verified this payload respects the interface required by the v3 config engine to do the following parameters changes:

USDC

- LTV: 81% -> **77%**
- Liquidation Threshold: 86% -> **80%**


<br>

USDC.e

- Supply cap: 150'000'000 USDC.e -> **26'000'000 USDC.e**
- Borrow cap: 100'000'000 USDC.e -> **24'000'000 USDC.e**
- LTV: 81% -> **77%**
- Liquidation Threshold: 86% -> **80%**
- Reserve factor: 10% -> **20%**
- Variable slope 1: 5% -> **7%**
- Variable slope 2: 60% -> **80%**

<br>

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
