# Proposal 66. TUSD and BUSD Aave V2 Rate Amendments.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=66](https://vote.onaave.com/proposal/?proposalId=66)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-tusd-and-busd-aave-v2-rate-amendments/16887](https://governance.aave.com/t/arfc-tusd-and-busd-aave-v2-rate-amendments/16887)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x71F2c0Ff83BEC8503a708c0bbDB30a26E83dB6C4#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal aims to lower the borrow rates for TUSD and BUSD following bad debt that is starting to get accrued. The concern is for that bad debt will keep rising too fast until it the protocol fees that are currently accrued will not be enough to cover it.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xebc78b8c1f396de3d6b69bc3fb6e5cfd2df967408a3c22d618dec53a12529a1d](https://etherscan.io/tx/0xebc78b8c1f396de3d6b69bc3fb6e5cfd2df967408a3c22d618dec53a12529a1d)

```
- proposalId: 66
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x9b463155a5aa776cee76c0946a81646c5d254e65ca58771c66de8b1277bab767
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
      "payloadId": "92" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x9b463155a5aa776cee76c0946a81646c5d254e65ca58771c66de8b1277bab767" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/66.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/66.md)

**Payload reports**

* Ethereum V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/92.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/92.md)

<br>

### Technical analysis

We have verified that for both assets, TUSD and BUSD, the rate strategies were altered to reflect a flat 10% yearly rate on variable rate, regardless of the utilization ratio.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
