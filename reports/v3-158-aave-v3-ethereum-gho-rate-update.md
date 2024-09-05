# Proposal 158. GHO Borrow Rate Update.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=158](https://vote.onaave.com/proposal/?proposalId=158)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-gho-stewards-gho-parameter-adjustments/17289/29](https://governance.aave.com/t/arfc-gho-stewards-gho-parameter-adjustments/17289/29)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xc8fC99B6E3dc4857ad08ffBABAe030b7cf031c21#code)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal sets new borrow interest rate value for gho to enhance competitiveness in the current market conditions.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x5ec2be31f5422f9295863e837c3d71ff8f1fceefa7a200a251e585d3c1c630c0](https://etherscan.io/tx/0x5ec2be31f5422f9295863e837c3d71ff8f1fceefa7a200a251e585d3c1c630c0)

```
- proposalId: 158
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x4d73cb1489c07aabc0c173ea556658910d965d10cb97796937510dcd2250fdc5
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
      "payloadId": "165" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x4d73cb1489c07aabc0c173ea556658910d965d10cb97796937510dcd2250fdc5" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/158.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/158.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/165.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/165.md)

<br>

### Technical analysis

We have verified that the payload changes the GHO interest rate strategy such that the borrow rate is decreased to 5.00% APR.


<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
