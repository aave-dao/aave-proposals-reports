# Proposal 206. Enable sUSDe/USDT Liquid E-Mode 


<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=206](https://vote.onaave.com/proposal/?proposalId=206)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-enable-susde-usdt-liquid-e-mode-on-core-instance/19939/2](https://governance.aave.com/t/arfc-enable-susde-usdt-liquid-e-mode-on-core-instance/19939/2)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xdc8CbF6976330B913ae0F430523555569B0C0aE0#code)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal seeks to enable sUSDe/USDT liquid E-Mode within the Aave Core Instance to enhance capital efficiency for borrowers using sUSDe as collateral to borrow USDT. The motivation stems from sUSDe’s proven utility as collateral for stablecoin borrowing, with the goal of expanding borrowing options and improving liquidity. By adding USDT to the sUSDe E-Mode, the proposal aims to attract more users, optimize sUSDe’s utilization, and bolster the Aave ecosystem’s liquidity offerings.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x26bcf9faddac3e5325ac77c7d3c67187531181a06446d32882814a76745168f2](https://etherscan.io/tx/0x26bcf9faddac3e5325ac77c7d3c67187531181a06446d32882814a76745168f2)

```
- proposalId: 206
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x5be8af9a90310435783626b0cf4cee0ec70d4c83781a73cb4da14bcfe0ac063b
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
      "payloadId": "211" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x5be8af9a90310435783626b0cf4cee0ec70d4c83781a73cb4da14bcfe0ac063b" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/206.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/206.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/211.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/211.md)


<br>

### Technical analysis

We have verified that the payload matches the proposal specifications, including enabling USDT borrowing in the sUSDe E-Mode with the appropriate configuration. The Seatbelt report has been reviewed and confirms compliance with Aave’s safety standards. Additionally, we confirm that the borrow bitmap configuration is correct and accurately reflects the intended changes.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

