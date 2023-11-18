# Proposal 370. Aave v3 Ethereum - WMATIC interest rate update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=370](https://app.aave.com/governance/proposal/?proposalId=370)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-wmatic-interest-rate-update/15309](https://governance.aave.com/t/arfc-wmatic-interest-rate-update/15309)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the interest rate strategy of wMATIC on Aave v3 Polygon.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x584b34ad8b976a4f20a5dd2868e1ddc001a6aadaec7ea78a5314722e99467816](https://etherscan.io/tx/0x584b34ad8b976a4f20a5dd2868e1ddc001a6aadaec7ea78a5314722e99467816)

```
- id: 370
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000890000000000000000000000000000000000000000000000000000000000000001000000000000000000000000401b5d0294e23637c18fcc38b1bca814cda2637c0000000000000000000000000000000000000000000000000000000000000007]
- withDelegatecalls: [false]
- startBlock: 18572695
- endBlock: 18591895
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xccfdf54fafdb4daeaa9e6284a43173ad78364158bd45915946393dcf7fe9d3df
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/370.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/370.md)

**Payloads report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/7.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/7.md)

<br>

### Technical analysis

We have verified that, as presented in the specification, the [proposal payload](https://polygonscan.com/address/0xF07633d14da9Dbca112ddE58C6d585CA8F4e845D#code#F1#L16) properly updates the following parameters of the WMATIC interest rate strategy:

- Variable borrow slope 1: 6.1% -> **5%**


The proposal is consistent with the description on the governance forum.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

