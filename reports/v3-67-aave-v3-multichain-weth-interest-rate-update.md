# Proposal 67. Update WETH IR on V3 Arbitrum and Optimism.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=67](https://vote.onaave.com/proposal/?proposalId=67)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-update-weth-ir-on-v3-arbitrum-and-optimism-02-16-2024/16644](https://governance.aave.com/t/arfc-chaos-labs-update-weth-ir-on-v3-arbitrum-and-optimism-02-16-2024/16644)

<br>

### Payloads

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0x9cd49bC5F12C23dac5e4b1772CD374128D8d2d8b#code#F1#L1)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x7a493B3E8b2B6d2252d4FcD9eB01425b5F311840#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal offer to reduce slope 1 of the WETH interest rate strategy to increase utilization rates and therefore revenue.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x6511adc27f0faaf4fa3c12a70fe0ab1ee019066c217aa98d364a0c90032bed47](https://etherscan.io/tx/0x6511adc27f0faaf4fa3c12a70fe0ab1ee019066c217aa98d364a0c90032bed47)

```
- proposalId: 67
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xb90aa7421fe73a9719f117a9c18bae08621e7bc79723a076d833d1b24cdfd371
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
      "payloadId": "21" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "20" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xb90aa7421fe73a9719f117a9c18bae08621e7bc79723a076d833d1b24cdfd371" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/67.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/67.md)

**Payload reports**

* Optimism V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/21.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/21.md)

* Arbitrum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/20.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/20.md)

<br>

### Technical analysis

We have verified that on both Optimism and Arbitrum the WETH's slope 1 was altered to 3.00% while keeping the rest of the parameters the same

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
