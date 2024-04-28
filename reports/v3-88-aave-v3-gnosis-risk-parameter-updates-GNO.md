# Proposal 88. Risk Parameter Updates GNO on V3 Gnosis.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=88](https://vote.onaave.com/proposal/?proposalId=88)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-gno-on-v3-gnosis/17340](https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-gno-on-v3-gnosis/17340)

<br>

### Payloads

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0xa50B2230e5F600b5790cc99D2CEb1268B1ee4AAE#code#F1#L28)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal increases liquidation threshold, LTV and debt ceiling of GNO asset on Aave-V3-Gnosis as part of observation done by Chaos Labs on GNO.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x858421581832f1d1dc3b64e9a9a4f7fe86381cf955ad145ddb4b5a3a22555f14](https://etherscan.io/tx/0x858421581832f1d1dc3b64e9a9a4f7fe86381cf955ad145ddb4b5a3a22555f14)

```
- proposalId: 88
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xc2ad821ca730c8e92d1c83412d94fb4b6daf1482662eafc88b055659a10ac52a
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "16" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xc2ad821ca730c8e92d1c83412d94fb4b6daf1482662eafc88b055659a10ac52a" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/88.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/88.md)

**Payload reports**

* Gnosis V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/16.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/16.md)


<br>

### Technical analysis

We have verified that the payload increases the liquidation threshold, LTV and debt ceiling of GNO by the following parameters:

    LTV: 45%

    LT: 50%

    Debt Ceiling: 2,000,000$

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
