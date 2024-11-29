# Proposal 209. USDS base rate and Slope1 Update.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=209](https://vote.onaave.com/proposal/?proposalId=209)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-usds-borrow-rate-update-on-core-and-prime-instances/19901/3](https://governance.aave.com/t/arfc-usds-borrow-rate-update-on-core-and-prime-instances/19901/3)

<br>

### Payloads

* Ethereum Core - [proposal payloads](https://etherscan.io/address/0x80Ef7fD7BFeE8aE54036f05f77e2efe201820a80#code)

* Ethereum Prime - [proposal payloads](https://etherscan.io/address/0x15E58f581fF19Bef412F9472Cd1fc453a0E084b8#code)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal adjusts the variable slope1 of USDS on the Ethereum Prime market to 9.25% and the base rate of USDS on Ethereum core market to 9.25%.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x863dcec92bdab4259cd6c1f8eb65e567416d0ed29e815cce715f613f3cfc7ce8](https://etherscan.io/tx/0x863dcec92bdab4259cd6c1f8eb65e567416d0ed29e815cce715f613f3cfc7ce8)

```
- proposalId: 209
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x1a9acbab30d3c9c381e899fb79433cf8bdb996bddb514b195baa32a085a84809
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
      "payloadId": "213" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x1a9acbab30d3c9c381e899fb79433cf8bdb996bddb514b195baa32a085a84809" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/192.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/209.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/213.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/213.md)

<br>

### Technical analysis

We have verified that the payload changes slope1 of USDS on the Ethereum prime market to 9.25% and base rate of USDS on core market to 9.25%

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

