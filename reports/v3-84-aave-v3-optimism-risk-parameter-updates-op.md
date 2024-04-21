# Proposal 84. Risk Parameter Updates - OP on V3 Optimism.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=84](https://vote.onaave.com/proposal/?proposalId=84)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-op-on-v3-optimism/17326](https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-op-on-v3-optimism/17326)

<br>

### Payloads

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0x571215CA49041F1aD21c58d4A7900CBd5a0C80EA#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal increases liquidation threshold and LTV of OP asset on Aave-V3-Optimism as part of observation done by Chaos Labs on OP's supply.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x01bedd4f795efc6fb2c0b266214a5a60bff4c5c531fdd7db78bd5b9566fef5b0](https://etherscan.io/tx/0x01bedd4f795efc6fb2c0b266214a5a60bff4c5c531fdd7db78bd5b9566fef5b0)

```
- proposalId: 84
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x0f8510f9117fbe8129a35eb4a72232ed483cb75a4650b7f81fedeafe17a24912
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "26" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x0f8510f9117fbe8129a35eb4a72232ed483cb75a4650b7f81fedeafe17a24912" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/84.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/84.md)

**Payload reports**

* Optimism V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/26.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/26.md)


<br>

### Technical analysis

We have verified that the payload increases the liquidation threshold and the LTV of OP by the following parameters:

    LTV: 50%

    LT: 60%

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
