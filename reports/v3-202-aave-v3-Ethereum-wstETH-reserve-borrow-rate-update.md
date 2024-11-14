# Proposal 202. wstETH Reserve Borrow Rate Update


<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=202](https://vote.onaave.com/proposal/?proposalId=202)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-weth-wsteth-borrow-rate-updates/19550/3](https://governance.aave.com/t/arfc-weth-wsteth-borrow-rate-updates/19550/3)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xBF0145791D3A396AE406e79B845D249b0ACE8b32#code)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This publication proposes reducing wstETH Slope1 parameter on the Main instance of Aave v3 on Ethereum. With the goal of encouraging user to borrow wstETH on the Main instance of Aave v3, the wstETH borrow rate will be lowered.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xc0485184e120d16fd02217f79d3e6dbf12b3810ed8e4716f07db28c901be15e4](https://etherscan.io/tx/0xc0485184e120d16fd02217f79d3e6dbf12b3810ed8e4716f07db28c901be15e4)

```
- proposalId: 202
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x26c178817d369782b4c7076cce3c4517265e104846a38c8ebd546d1474cd5c75
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "1", 
      "accessLevel": "1", 
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5", 
      "payloadId": "208" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x26c178817d369782b4c7076cce3c4517265e104846a38c8ebd546d1474cd5c75" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/202.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/202.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/208.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/208.md)

<br>

### Technical analysis

We have verified that the proposal payload changes to the specified baseVariableBorrowRate and slope1 values.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

