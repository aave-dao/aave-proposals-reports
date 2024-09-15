# Proposal 165. Listing USDS and SUSDS Part I.


<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=165](https://vote.onaave.com/proposal/?proposalId=165)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-onboard-usds-and-susds-to-aave-v3/18987](https://governance.aave.com/t/arfc-onboard-usds-and-susds-to-aave-v3/18987)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x2749Ef5641B90DCD17Ee2C0cbFbbA5b440e14fec#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:gem: :new: asset-listing

<br>

### Context

This proposal onboard USDS and sUSDS, the rebranded DAI and sDAI tokens to Aave v3 Ethereum Main Pool.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x7a1c18915c4533e8fa7a6ace891e19423084e6fcf7395a2535dd71d2fd4fb6d8](https://etherscan.io/tx/0x7a1c18915c4533e8fa7a6ace891e19423084e6fcf7395a2535dd71d2fd4fb6d8)

```
- proposalId: 165
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xc72ab6b294d06516b1469324315f8e92e1bd78d61c250e9628f9d21b6ce62e6f
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
      "payloadId": "173" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xc72ab6b294d06516b1469324315f8e92e1bd78d61c250e9628f9d21b6ce62e6f" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/165.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/165.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/173.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/173.md)

<br>

### Technical analysis

We have verified that the payload list the new USDS and sUSDS tokens as specified in the AIP.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
