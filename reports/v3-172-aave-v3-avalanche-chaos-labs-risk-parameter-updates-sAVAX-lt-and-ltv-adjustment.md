# Proposal 172. Chaos Labs Risk Parameter Updates - sAVAX LT/LTV Adjustment.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=172](https://vote.onaave.com/proposal/?proposalId=172)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-savax-lt-ltv-adjustment/18995](https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-savax-lt-ltv-adjustment/18995)

<br>

### Payloads

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xa8C2bf37595693Db9cE42B07005916ECd6502581/contract/43114/code)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal increases the ltv and lt of sAVAX and AVAX_CORRELATED E-Mode on Aave-V3-Avalanche market.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x78267c48f60ad5e98194ff30f6266744015242f0352bc6b76f051a0886693b65](https://etherscan.io/tx/0x78267c48f60ad5e98194ff30f6266744015242f0352bc6b76f051a0886693b65)

```
- proposalId: 172
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x6844f45501f65809e0dc1db55cc86a1795e2636b6b64eb4af107d4b901af76e4
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "54" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x6844f45501f65809e0dc1db55cc86a1795e2636b6b64eb4af107d4b901af76e4" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/172.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/172.md)

**Payload reports**

* Avalanche - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/54.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/54.md)

<br>

### Technical analysis

We have confirmed that the payload successfully increase sAVAX LTV from 40% to 50% and it's LT from 45% to 55% and that AVAX_CORRELATED eMode's LTV has increased from 92.5% to 93%.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

