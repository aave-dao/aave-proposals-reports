# Proposal 407. Treasury Management - TokenLogic & Karpatkey engagement

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=407](https://app.aave.com/governance/proposal/?proposalId=407)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-tokenlogic-karpatkey-service-provider-partnership/15755](https://governance.aave.com/t/arfc-tokenlogic-karpatkey-service-provider-partnership/15755)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposal approves a 6-months engagement for Aave with a partnership of TokenLogic & Karpatkey, for a total of 400'000 GHO streamed over that period.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xeb19f137573189a51ec728eec543a34957ff998eec1974f9481f98948f906829](https://etherscan.io/tx/0xeb19f137573189a51ec728eec543a34957ff998eec1974f9481f98948f906829)

```
- id: 407
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dabad81af85554e9ae636395611c58f7ec1aaec50000000000000000000000000000000000000000000000000000000000000027]
- withDelegatecalls: [false]
- startBlock: 18797385
- endBlock: 18816585
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x87923c47c82b1e54bb17e847142e86de2cd7d9df63d79cfc51037ca989cd44e5
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/407.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/407.md)

**Payloads reports**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/39.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/39.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x485CDe091918e1EaC67495a73DBa7bbcf1Da4F86#code#F1#L15) does the following:

1. Creates 2 streams, one of ~220'000 GHO and another of ~180'000 GHO, from the Aave Ethereum Collector to the addresses defined as `STREAM_ONE_RECEIVER` and `STREAM_TWO_RECEIVER`, with a duration of 180 days and starting at the time of proposal execution.

2. Cancel stream `100017` of the TokenLogic Orbit program, considering this next engagement.


We have confirmed the amount and duration is consistent with what is defined on the Aave governance forum, Snapshot and AIP.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
