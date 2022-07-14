# Proposal 88. Sigma Prime - Security Assessment Services for Aave

<br>

### Voting link
[https://app.aave.com/governance/proposal/?proposalId=88](https://app.aave.com/governance/proposal/?proposalId=88)

### Governance forum discussion
[https://governance.aave.com/t/sigma-prime-security-assessment-services-for-aave/8518](https://governance.aave.com/t/sigma-prime-security-assessment-services-for-aave/8518)

<br>

## BGD analysis

### Proposal types

:credit_card: funds-allowance

:money_with_wings: funds-release

### Context

This proposal approves an engagement of the Aave community with the security firm [Sigma Prime](https://sigmaprime.io/) during one year, involving a total payment of 1,296,000 USD.
This proposal transfers to Sigma Prime a first tranche of 648,000 USD (in aUSDC and aUSDT), and creates a delayed payment for other 648,000 USD after 12 months. 

### Proposal creation
Transaction: [https://etherscan.io/tx/0x03ca1aff06591760eae2a7aa454cd3e4364166802fe79b34b4f3880cc577179c](https://etherscan.io/tx/0x03ca1aff06591760eae2a7aa454cd3e4364166802fe79b34b4f3880cc577179c)
```
- id: 88
- creator: 0xb86cb4d6a47c7d50c232793cd61707ad60377a75
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xe8ea74754dce51168102e820424f7e7f74c5be3e]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 15140137
- endBlock: 15159337
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xec8fc43da4504c01c0aaf85dec47289e5d3abcc3bc08b90c3018c15acd373644
```

### Aave Seatbelt report
[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/088.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/088.md)

### Technical analysis

From a technical perspective, we have verified that the proposal payload does the following:

1. Transfers 324,000 aUSDC and 324,000 aUSDT from the [Aave V2 Ethereum Collector](https://etherscan.io/address/0x464C71f6c2F760DdA6093dCB91C24c39e5d6e18c) to the Sigma Prime recipient address. That is half and half of the 648,000 USD upfront amount, defined in the engagement.

2. Schedules 2 delayed payments of 324,000 aUSDC and 324,000 aUSDT, also from the [Aave V2 Ethereum Collector](https://etherscan.io/address/0x464C71f6c2F760DdA6093dCB91C24c39e5d6e18c), to the Sigma Prime recipient address, to be claimable in 365 days. This is technically done by using the streaming capabilities of the Aave V2 Ethereum Collector, creation 2 streams with delay of 365 days and duration of 1s after that delay, becoming factually a delayed payment. It is important to highlight that the comment `// 6 months stream, starting 6 months from now` on the proposal payload is not correct (should indicated 12 months), but the logic actually is.


### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

:white_check_mark: Only one payload used via delegatecall

