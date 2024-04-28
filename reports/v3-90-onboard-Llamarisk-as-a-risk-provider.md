# Proposal 90. Onboard Llamarisk as a Risk Provider.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=90](https://vote.onaave.com/proposal/?proposalId=90)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-onboard-new-risk-service-provider/17348](https://governance.aave.com/t/arfc-onboard-new-risk-service-provider/17348)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x2C3f5D3EB59074631DC33763D903afD8426868C2#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:bank: payment stream

<br>

### Context

This proposal is a stream creation of 250,000$ payed in GHO which will officially onboard the LlamaRisk team as Aave's second Risk Service Provider.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x1693ac72d9946f7ba0c9b1170cd8e2171553d5922e636e55a2b707d49df77600](https://etherscan.io/tx/0x1693ac72d9946f7ba0c9b1170cd8e2171553d5922e636e55a2b707d49df77600)

```
- proposalId: 90
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xe78fa71ec1e15432e74698a4e94c0120bef1b2817343e6d55296b3f53ef63386
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
      "payloadId": "114" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xe78fa71ec1e15432e74698a4e94c0120bef1b2817343e6d55296b3f53ef63386" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/90.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/90.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/114.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/114.md)

<br>

### Technical analysis

We have verified that the following payments were made to the address provided by LlamaRisk.

Stream to the benefit of LlamaRisk:
- 250,000 GHO streamed over a period of 180 days, starting at execution. 

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
