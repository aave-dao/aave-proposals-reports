# Proposal 394. Aave v3 Base - listing of wstETH

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=394](https://app.aave.com/governance/proposal/?proposalId=394)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-onboarding-wsteth-to-aave-v3-on-base-network/15510](https://governance.aave.com/t/arfc-onboarding-wsteth-to-aave-v3-on-base-network/15510)

<br>

## BGD analysis

<br>

### Proposal types

:gem: :new: asset-listing

:crystal_ball: oracle-addition

<br>

### Context

This proposal lists wstETH on the Aave v3 Base pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xc8d3d3ad2cfdf4c49236b8ed63d21ba5732f10dec74d475f18d01657c1ae040a](https://etherscan.io/tx/0xc8d3d3ad2cfdf4c49236b8ed63d21ba5732f10dec74d475f18d01657c1ae040a)

```
- id: 394
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x000000000000000000000000000000000000000000000000000000000000210500000000000000000000000000000000000000000000000000000000000000010000000000000000000000002dc219e716793fb4b21548c0f009ba3af753ab010000000000000000000000000000000000000000000000000000000000000003]
- withDelegatecalls: [false]
- startBlock: 18718855
- endBlock: 18738055
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x97cb967a0f93cdfd7170e34aefc145a080c01001f120809f474fe28bdc68640f
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/394.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/394.md)

**Payload report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/3.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/3.md)


<br>

### Technical analysis

We have verified the proposal uses correctly a.DI to communicate with Base.

The [proposal payload](https://basescan.org/address/0x3b0b255e648D6680a6cf1A5aF92c73240e13C69d#code#F1#L18) correctly uses the BGD's Aave Config Engine of Aave v3 Base, in this case, its listing features.

We have verified this payload respects the interface required by the v3 config engine and effectively configures the wstETH asset with the following initial parameters:

- The asset is enabled for borrowing and the interest rate strategy follows the parameters on the forum:
  - Base variable borrow: 0%
  - Variable borrow slope 1: 7%
  - Variable borrow slope 2: 300%
  - Optimal point: 45%
- The asset is enabled as collateral with the following configuration:
  - LTV: 71%
  - Liquidation Threshold: 76%
  - Liquidation Bonus: 6%
  - Liquidation Protocol Fee: 10%
- Reserve Factor: 15%
- Supply cap: 4'000 wstETH
- Borrow cap: 400 wstETH
- e-mode category: ETH correlated (1)
- No isolation mode
- Flashlonable
- Not enabled for borrowing on isolation

The oracle used is a BGD sync adapter [wstETH/ETH/USD](https://basescan.org/address/0x945fd405773973d286de54e44649cc0d9e264f78#readContract#F8).

The initial configuration is completely aligned with the description on the Aave governance forum.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

