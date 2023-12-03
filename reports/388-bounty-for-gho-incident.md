# Proposal 388. Bounty for GHO incident

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=388](https://app.aave.com/governance/proposal/?proposalId=388)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-gho-bounty-for-integration-issue-detection/15296](https://governance.aave.com/t/arfc-gho-bounty-for-integration-issue-detection/15296)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposal approves a payment of 50'000 GHO to a community member that collaborated in the detection of the GHO incident on August 25th.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x013917ed90ec91ee11e34d3983b02617966c9dec7e9889e5bea74714d99317f1](https://etherscan.io/tx/0x013917ed90ec91ee11e34d3983b02617966c9dec7e9889e5bea74714d99317f1)

```
- id: 388
- creator: 0x38392004bfbef356a1355b71ab045fd64766b65f
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dabad81af85554e9ae636395611c58f7ec1aaec50000000000000000000000000000000000000000000000000000000000000019]
- withDelegatecalls: [false]
- startBlock: 18686172
- endBlock: 18705372
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xfc641fbbfb34ae3e4c43979420b4bf64537077d883b817a6808b38ff662577bf
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/388.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/388.md)

**Payload report**

*Due to some problems with Aave Seatbelt, this report is not available*

<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x5107F3274893dAF384241370CB84c9991780A786#code#F1#L13) properly transfers 50'000 GHO from the Aave v3 Collector to the address defined as [RECEIVER](https://etherscan.io/address/0x7D51910845011B41Cc32806644dA478FEfF2f11F).

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
