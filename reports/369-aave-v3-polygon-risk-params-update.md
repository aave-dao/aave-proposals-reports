# Proposal 369. Aave v3 Polygon - CRV risk parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=369](https://app.aave.com/governance/proposal/?proposalId=369)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-crv-aave-v3-polygon-lt-reduction-10-28-2023/15259](https://governance.aave.com/t/arfc-chaos-labs-crv-aave-v3-polygon-lt-reduction-10-28-2023/15259)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal adjusts the Liquidation Threshold parameter of CRV on Aave v3 Polygon.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x5efe86bef5923b06c930ddca3b9323858c51a08dd71b6a872b10b2bcacf1d406](https://etherscan.io/tx/0x5efe86bef5923b06c930ddca3b9323858c51a08dd71b6a872b10b2bcacf1d406)

```
- id: 369
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000890000000000000000000000000000000000000000000000000000000000000001000000000000000000000000401b5d0294e23637c18fcc38b1bca814cda2637c0000000000000000000000000000000000000000000000000000000000000006]
- withDelegatecalls: [false]
- startBlock: 18571412
- endBlock: 18590612
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xb104d0e864fe799782bcca3f0c509021868c1963ab4d2b3bc4a9c710ee7e5483
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/369.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/369.md)

**Payloads report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/6.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/6.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://polygonscan.com/address/0xCfff816b036423BeEaDc20a147586168d88b7CdA#code#F1#L12) does the following changes by interacting with the BGD Aave v3 Polygon Config Engine:

CRV
- Liquidation Threshold: 65% -> **50%**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
