# Proposal 32. MaticX Supply Cap Increase in Polygon V3

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=32](https://vote.onaave.com/proposal/?proposalId=32)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-maticx-supply-cap-increase-in-polygon-v3/16449](https://governance.aave.com/t/arfc-maticx-supply-cap-increase-in-polygon-v3/16449)

<br>

### Payloads

* Polygon - [proposal payloads](https://polygonscan.com/address/0xEa0BA2aE9E9670B52ce74606e7ED92eaD2013A98#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal increases MaticX supply cap to allow more supply, and thereby borrowing, of the token due to high demand.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xca330bad40469a97586deb879c4f5d888e19c4d2353df3b11bbc1e345251c50f](https://etherscan.io/tx/0xca330bad40469a97586deb879c4f5d888e19c4d2353df3b11bbc1e345251c50f)

```
- proposalId: 32
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xa68d7be09ce1026a06a83089bfc3b6317f4926c2f710aa3961e0dd7acbff767d
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "37" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xa68d7be09ce1026a06a83089bfc3b6317f4926c2f710aa3961e0dd7acbff767d" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/32.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/32.md)

**Payload reports**

* Polygon V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/37.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/37.md)

<br>

### Technical analysis

We have verified that the payload increase the supply cap of MaticX from 62M to 75M

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
