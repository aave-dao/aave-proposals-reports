# Proposal 107. SUSD risk parameters update.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=107](https://vote.onaave.com/proposal/?proposalId=107)

<br>

### Governance forum discussion

[https://governance.aave.com/t/susd-depeg-update-05-16-2024/17719](https://governance.aave.com/t/susd-depeg-update-05-16-2024/17719)

<br>

### Payloads

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0x9259C93a5044186d3bdC435b5b516B7fbcc27Cac#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal suggests risk parameters change following a de-peg of SUSD in recent time.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x5850c230e744825a4f04e58e0a292773eed187d8e8c8449b62b7862351ae6f2d](https://etherscan.io/tx/0x5850c230e744825a4f04e58e0a292773eed187d8e8c8449b62b7862351ae6f2d)

```
- proposalId: 107
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x7ae0c2025ef34dd6e9b64fe2febd4687d3a63bb83bc15a5aa7dd7756176a2404
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
      "payloadId": "31" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x7ae0c2025ef34dd6e9b64fe2febd4687d3a63bb83bc15a5aa7dd7756176a2404" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/107.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/107.md)

**Payload reports**

* Optimism V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/31.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/31.md)

<br>

### Technical analysis

We have verified that the LTV of the SUSD reserve was modified to 0%. No other changes were introduced in this AIP.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
