# Proposal 117. Adjusting Interest Rate Curve for weETH on Arbitrum.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=117](https://vote.onaave.com/proposal/?proposalId=117)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-adjusting-interest-rate-curve-for-weeth-on-arbitrum/17804](https://governance.aave.com/t/arfc-adjusting-interest-rate-curve-for-weeth-on-arbitrum/17804)

<br>

### Payloads

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x1d57887F9FE787cD1a843Bd539922e9DFEb2Ba35#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal suggests interest rate parameters changes to weETH in order to align the parameters of the asset with other markets and optimize the utilization rates and improve revenue for the DAO.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xd6a34d60d5c58f1a384ab791878dd153c82384ae99bc0aad727a2695798ee51b](https://etherscan.io/tx/0xd6a34d60d5c58f1a384ab791878dd153c82384ae99bc0aad727a2695798ee51b)

```
- proposalId: 117
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x802a4a10c5927a267eabe8f57cc85f6f240293399d08473ce283a4c960460a42
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "30" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x802a4a10c5927a267eabe8f57cc85f6f240293399d08473ce283a4c960460a42" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/117.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/117.md)

**Payload reports**

* Arbitrum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/30.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/30.md)

<br>

### Technical analysis

We have verified that the payload modifies the optimal utilization rate and the reserve factor of weETH on Arbitrum-V3 to the following parameters:

- Uoptimal: 35%

- reserve factor: 45%

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
