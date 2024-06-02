# Proposal 114. Chaos Labs Parameter Recommendations sUSD on V3 Optimism.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=114](https://vote.onaave.com/proposal/?proposalId=114)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-parameter-recommendations-susd-on-v3-optimism-05-23-2024/17779](https://governance.aave.com/t/arfc-chaos-labs-parameter-recommendations-susd-on-v3-optimism-05-23-2024/17779)

<br>

### Payloads

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0x5594521a5132Faf674552cfc6387B75cF10F9924#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal suggests risk parameters changes to sUSD following the depeg of the asset, freeze of the market on Aave and repeg to reflect the current state of the market.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xa545089be8b8708f48233e8069ae8483605c0399f507d97192989583d2ef5fcf](https://etherscan.io/tx/0xa545089be8b8708f48233e8069ae8483605c0399f507d97192989583d2ef5fcf)

```
- proposalId: 114
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x880874b26e761785fe82e63387b1c4eeb48375ed71d3333f245076b7fc636183
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
      "payloadId": "33" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x880874b26e761785fe82e63387b1c4eeb48375ed71d3333f245076b7fc636183" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/114.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/114.md)

**Payload reports**

* Optimism V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/33.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/33.md)

<br>

### Technical analysis

We have verified that the payload unfreeze the sUSD market, as well as updates the risk parameters of sUSD to following values:

Asset Parameters:
- LTV: 60%
- LT: 70%
- Supply Cap: 7M sUSD
- Borrow Cap: 5.6M sUSD

E-mode Parameters:
- LTV: 90%
- LT: 93%

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
