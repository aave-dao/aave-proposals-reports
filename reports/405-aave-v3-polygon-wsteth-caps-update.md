# Proposal 405. Aave v3 Polygon - wstETH supply cap update

<br>


### Voting link

[https://app.aave.com/governance/proposal/?proposalId=405](https://app.aave.com/governance/proposal/?proposalId=405)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-increase-supply-and-borrow-caps-at-100-utilization-december-2023/15754](https://governance.aave.com/t/arfc-increase-supply-and-borrow-caps-at-100-utilization-december-2023/15754)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal increases the supply cap of wstETH on Aave v3 Polygon.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x1cf6abd70ff8f6633213af9e6379920948eff41548c700c7cc88c850ce0d9920](https://etherscan.io/tx/0x1cf6abd70ff8f6633213af9e6379920948eff41548c700c7cc88c850ce0d9920)

```
- id: 405
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000890000000000000000000000000000000000000000000000000000000000000001000000000000000000000000401b5d0294e23637c18fcc38b1bca814cda2637c0000000000000000000000000000000000000000000000000000000000000015]
- withDelegatecalls: [false]
- startBlock: 18789881
- endBlock: 18809081
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xfb4ad1c5102d089d7c69751f6decf435339e6f1be8d828e89f434976b2a55b69
```

<br>

### Aave Seatbelt reports

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/405.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/405.md)

**Payload report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/21.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/21.md)

<br>

### Technical analysis

From a technical perspective, we have verified the [proposal payload](https://polygonscan.com/address/0x31e3eE4DfbA3EBF9A581F48f2865f417d85BB573#code#F1#L15) correctly uses the BGD's Aave Config Engine of Aave v3 Polygon, in this case, to update the following supply cap:

wstETH
- Supply cap: 3'450 wstETH -> **4'370 wstETH**

<br>

The proposal is consistent with the description in the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
