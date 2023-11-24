# Proposal 375. Aave v3 Polygon, Avalanche, Optimism, Arbitrum - Deprecation of MAI

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=376](https://app.aave.com/governance/proposal/?proposalId=376)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-gauntlet-recommendation-for-mai-mimatic-deprecation/15119](https://governance.aave.com/t/arfc-gauntlet-recommendation-for-mai-mimatic-deprecation/15119)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal progress on the offboarding of MAI (miMATIC) from all Aave instances, by changing risk parameters and rate strategies.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x43d2a49ef54d84dabd09fce9c53988b8e894b98b87775ec9fd34d63e603ac8fb](https://etherscan.io/tx/0x43d2a49ef54d84dabd09fce9c53988b8e894b98b87775ec9fd34d63e603ac8fb)

```
- id: 376
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7,0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7,0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7,0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0,0,0,0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40)),forwardPayloadForExecution((uint256,uint8,address,uint40)),forwardPayloadForExecution((uint256,uint8,address,uint40)),forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000890000000000000000000000000000000000000000000000000000000000000001000000000000000000000000401b5d0294e23637c18fcc38b1bca814cda2637c0000000000000000000000000000000000000000000000000000000000000009,0x000000000000000000000000000000000000000000000000000000000000a86a00000000000000000000000000000000000000000000000000000000000000010000000000000000000000001140cb7cafacc745771c2ea31e7b5c653c5d0b800000000000000000000000000000000000000000000000000000000000000006,0x000000000000000000000000000000000000000000000000000000000000000a00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000e1a3af1f9cc76a62ed31ededca291e63632e7c40000000000000000000000000000000000000000000000000000000000000003,0x000000000000000000000000000000000000000000000000000000000000a4b1000000000000000000000000000000000000000000000000000000000000000100000000000000000000000089644ca1bb8064760312ae4f03ea41b05da3637c0000000000000000000000000000000000000000000000000000000000000003]
- withDelegatecalls: [false,false,false,false]
- startBlock: 18622155
- endBlock: 18641355
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xb2fcb5da149a326de38268779244b13e824e7b5e3426d37f76865e9e41dde43e
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://raw.githubusercontent.com/bgd-labs/seatbelt-for-ghosts/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/376.md](https://raw.githubusercontent.com/bgd-labs/seatbelt-for-ghosts/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/376.md)

**Payloads reports**

- Polygon

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/9.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/9.md)

- Avalanche

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/6.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/6.md)

- Optimism

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/3.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/3.md)

- Arbitrum

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/3.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/3.md)

<br>

### Technical analysis

We have verified that, per network, the following changes are applied to MAI by using the Aave BGD config engine.

**[Polygon](https://polygonscan.com/address/0x47a200a4805297c396aE73FFD52044D1Edb261bA#code#F1#L16)**

- Liquidation threshold: 80% -> **1%**
- Reserve factor: 20% -> **95%**
- Optimal point: 80% -> **45%**
- Variable slope 2: 75% -> **300**

**[Avalanche](https://snowtrace.io/address/0xf7C3350757DE224bdB2b77A3943C8667aCEE3d37#code#F1#L16)**

- Freeze reserve
- LTV: 75% -> **0%**
- Liquidation threshold: 80% -> **1%**
- Reserve factor: 20% -> **95%**
- Optimal point: 80% -> **45%**
- Variable slope 2: 75% -> **300**

**[Optimism](https://optimistic.etherscan.io/address/0xf8bC2a699559c96D48cf1e6F70aa2e67508C2aE9#code#F1#L16)**

- Liquidation threshold: 80% -> **65%**
- Reserve factor: 20% -> **95%**
- Optimal point: 80% -> **45%**
- Variable slope 2: 75% -> **300**

**[Arbitrum](https://arbiscan.io/address/0x0cB2535D00cddFae5Ed1aFf2e5a0239fC947D17d#code#F1#L16)**

- Liquidation threshold: 80% -> **1%**
- Reserve factor: 20% -> **95%**
- Optimal point: 80% -> **45%**
- Variable slope 2: 75% -> **300**

<br>

---

<br>


The proposal is diverges slightly from the description in the forum, but only due to technical limitations of not being able to set LT to 0.
The AIP description is consistent with the payloads.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

