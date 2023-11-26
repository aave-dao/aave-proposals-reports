# Proposal 381. Aave v3 Ethereum - GHO interest rate strategy update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=381](https://app.aave.com/governance/proposal/?proposalId=381)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-increase-gho-borrow-rate-to-5-22-on-aave-v3/15632](https://governance.aave.com/t/arfc-increase-gho-borrow-rate-to-5-22-on-aave-v3/15632)

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

Transaction: [https://etherscan.io/tx/0x152152468e377fee7333ce6625b9673b4b2ad962961d05643678a848569e275d](https://etherscan.io/tx/0x152152468e377fee7333ce6625b9673b4b2ad962961d05643678a848569e275d)

```
- id: 381
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dabad81af85554e9ae636395611c58f7ec1aaec50000000000000000000000000000000000000000000000000000000000000016]
- withDelegatecalls: [false]
- startBlock: 18636650
- endBlock: 18655850
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x4977ecf7075c1e4d30973c4e1d34c1d2d3a1c989ae5da116a6ad951d974c4f65
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/381.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/381.md)

**Payloads report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/22.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/22.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x0d66E00c5b876d661C3261e82a99BfFaD1ebE147#code#F1#L12) properly updates the GHO interest rate strategy with [this one](https://etherscan.io/address/0xE6e780D77b883E9a5eC84f7baA6BF4DB43177Fa7#code#F1#L15).

This will change the GHO (fixed) rate to 5.22%, from the current 4.72%.

The proposal is consistent with the discussions on the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
