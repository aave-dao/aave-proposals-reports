# Proposal 72. Upgrade AMPL implementation.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=72](https://vote.onaave.com/proposal/?proposalId=72)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-aampl-interim-distribution/17184](https://governance.aave.com/t/arfc-aampl-interim-distribution/17184)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x692f53C7CBF00769eCf65c0e2adeD52324a3767e)

<br>

## Certora analysis

<br>

### Proposal types

:scroll::small_red_triangle: contract upgrade
:wrench: :bar_chart: configuration update

<br>

### Context

This proposal upgrades the aAMPL implementation due to problem that came up. In addition, it updates the IR strategy of the token on V2 Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x4303a2f751f1957f14a275cdefc88b70bc8535d55832a460e02d0cabbf0ef7c8](https://etherscan.io/tx/0x4303a2f751f1957f14a275cdefc88b70bc8535d55832a460e02d0cabbf0ef7c8)

```
- proposalId: 72
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0xaa46d2cf629d68cc84bcc83156b2fd8e54819c5e848c229c7e62d1f6212886cc
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
      "payloadId": "99" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xaa46d2cf629d68cc84bcc83156b2fd8e54819c5e848c229c7e62d1f6212886cc" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/72.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/72.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/99.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/99.md)

<br>

### Technical analysis

We have verified that the payload upgrades the aAMPL implementation, as well as alters the IR strategy to reflect a change in slope 2 to 300%.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
