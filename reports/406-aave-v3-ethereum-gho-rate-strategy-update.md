# Proposal 406. Aave v3 Ethereum - GHO interest rate strategy update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=406](https://app.aave.com/governance/proposal/?proposalId=406)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-increase-gho-borrow-rate-100-bps-to-6-35-on-aave-v3/15744](https://governance.aave.com/t/arfc-increase-gho-borrow-rate-100-bps-to-6-35-on-aave-v3/15744)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the interest rate strategy of GHO on Aave v3 Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xbe90473b807916dd4237f8c963f8cd1f73a56fbf679bb330aa14ed12aac892ab](https://etherscan.io/tx/0xbe90473b807916dd4237f8c963f8cd1f73a56fbf679bb330aa14ed12aac892ab)

```
- id: 406
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dabad81af85554e9ae636395611c58f7ec1aaec50000000000000000000000000000000000000000000000000000000000000025]
- withDelegatecalls: [false]
- startBlock: 18789888
- endBlock: 18809088
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xfd84f925c89bfede52d221346bb98df66f7849665e18b57e5843ac92ff410c6a
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/406.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/406.md)

**Payloads report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/37.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/37.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x888Ffb3949ba4bCCCa176E13d8b3843db1E6a18D#code#F1#L12) properly updates the GHO interest rate strategy with [this one](https://etherscan.io/address/0x00524e8e4c5fd2b8d8aa1226fa16b39cad69b8a0).

This will change the GHO (fixed) rate to 6.22%, from the current 5.22%.

The proposal is consistent with the discussions on the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
