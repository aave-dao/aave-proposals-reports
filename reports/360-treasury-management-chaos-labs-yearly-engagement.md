# Proposal 360. Treasury Management - Chaos Labs yearly engagement

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=360](https://app.aave.com/governance/proposal/?proposalId=360)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-aave-risk-management-renewal/15234](https://governance.aave.com/t/arfc-chaos-labs-aave-risk-management-renewal/15234)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposal approves yearly renewal of the engagement Aave <> Chaos Labs, for a total of $1'600'000 in a continuous stream.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x5c0637817474def4c84fbc98fe29336b4a1c1c75401140d10e28bc4a01e3957e](https://etherscan.io/tx/0x5c0637817474def4c84fbc98fe29336b4a1c1c75401140d10e28bc4a01e3957e)

```
- id: 360
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dabad81af85554e9ae636395611c58f7ec1aaec50000000000000000000000000000000000000000000000000000000000000009]
- withDelegatecalls: [false]
- startBlock: 18528712
- endBlock: 18547912
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xa29f92cb29c3bd4bf1400c267ad1ceda4b58c45a4977a8175c2f9c38748b67da
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/360.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/360.md)

**Payloads reports**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/9.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/9.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xfb1163CD80850CD107bB134C15E5dfDF284F63FE#code#F1#L14) properly uses the interim governance v2.5 system, and does the following:

1. Creates an stream of ~800'000 GHO from the Aave Ethereum Collector to the address defined as [CHAOS_LABS_TREASURY](https://etherscan.io/address/0xbC540e0729B732fb14afA240aA5A047aE9ba7dF0), with a duration of 365 days and starting at the time of proposal execution.

2. Creates an stream of ~800'000 aUSDT v2 from the Aave Ethereum Collector, with the same duration and recipient parameters as the previous.

We have confirmed the amount and duration is consistent with what is defined on the Aave governance forum, Snapshot and AIP.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
