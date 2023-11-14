# Proposal 365. Aave v3 Ethereum - GHO interest rate strategy update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=365](https://app.aave.com/governance/proposal/?proposalId=365)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-gho-increase-borrow-rate/15271](https://governance.aave.com/t/arfc-gho-increase-borrow-rate/15271)

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

Transaction: [https://etherscan.io/tx/0xe7fed0c69c31d879f0f60a3b7226ad3cb2c4a22e534d310ac868a27cd84837a7](https://etherscan.io/tx/0xe7fed0c69c31d879f0f60a3b7226ad3cb2c4a22e534d310ac868a27cd84837a7)

```
- id: 365
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dabad81af85554e9ae636395611c58f7ec1aaec5000000000000000000000000000000000000000000000000000000000000000a]
- withDelegatecalls: [false]
- startBlock: 18541317
- endBlock: 18560517
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x8168f0a661eb7c947924a6f9a83bfc5c977daded01fb134fafb4620b964f9ad3
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/365.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/365.md)

**Payloads report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/10.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/10.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xa2de136bfd7ff998c825229fdebfaf77726c43ec#code#F22#L12) properly updates the GHO interest rate strategy with [this one](https://etherscan.io/address/0xe7c0ae65f7d52e121654eea0a57b4af0894f6d27#code#F1#L15).

This will change the GHO (fixed) rate to 4.72%, from the current 3%.

The proposal is consistent with the discussions on the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
