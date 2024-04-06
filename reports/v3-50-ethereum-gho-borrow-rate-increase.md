# Proposal 50. GHO Borrow Rate Increase.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=50](https://vote.onaave.com/proposal/?proposalId=50)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-increase-gho-borrow-rate-08-03-2024/16885](https://governance.aave.com/t/arfc-increase-gho-borrow-rate-08-03-2024/16885)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xEaB5ffECC90082d75E0a1dE43Dddb1eC4ac9Bb9f#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update
:scroll::small_red_triangle: contract upgrade

<br>

### Context

This proposal increases the gho borrowing rate on the protocol to align with the market rates in order to support the current gho pegging.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xcf402b84c07e3f95501da78ff8acd241f6ffa025f0fbadb0d6c791aeb2ed1e2f](https://etherscan.io/tx/0xcf402b84c07e3f95501da78ff8acd241f6ffa025f0fbadb0d6c791aeb2ed1e2f)

```
- proposalId: 50
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xef89c76c2e9d4112bbe6851449cf82d092e2175cf6017481b62708c3954f7a60
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
      "payloadId": "76" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xef89c76c2e9d4112bbe6851449cf82d092e2175cf6017481b62708c3954f7a60" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/50.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/50.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/76.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/76.md)

<br>

### Technical analysis

We have verified that the payload changes the GHO interest rate strategy such that the borrow rate is increased to 7.92% APR without changing the max discount rate.

<br>

The proposal is consistent with the description on the governance forum. It also follows an accelerated procedure following the approval of AIP-381 which pre-approved ACI to perform changes in GHO borrow rate up to 1% with some limitations. [see AIP here](https://governance-v2.aave.com/governance/proposal/381/).

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
