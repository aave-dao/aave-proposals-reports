# Proposal 99. ACI Ad Astra.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=99](https://vote.onaave.com/proposal/?proposalId=99)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-aci-phase-iii-ad-astra/17515](https://governance.aave.com/t/arfc-aci-phase-iii-ad-astra/17515)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x69624318576E18f454266b51e5a0b4F5242a582d#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:bank: payment stream

<br>

### Context

This proposal is a stream creation of 1,000,000$ payed in GHO which will be a continuation of the collaboration with the Aave-chan Initiative (ACI) for a period of 365 days.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xf50c946bf685a19b94b62451306e7e729ebc31eb53a0107e116fafdd1fe98fd5](https://etherscan.io/tx/0xf50c946bf685a19b94b62451306e7e729ebc31eb53a0107e116fafdd1fe98fd5)

```
- proposalId: 99
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x0a1a2e345c28bb360a2b0b5ac3ec2442cf5fc9f0b1721577af7b55182f0db21f
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
      "payloadId": "121" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x0a1a2e345c28bb360a2b0b5ac3ec2442cf5fc9f0b1721577af7b55182f0db21f" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/99.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/99.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/121.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/121.md)

<br>

### Technical analysis

We have verified that the following payments were made to the address provided by ACI.

Stream to the benefit of ACI:
- 1,000,000 GHO streamed over a period of 365 days, starting at execution. 

Transfer 16,440$ (2740$ per day) of GHO to reflect on the work done until the payload executes - from May 5 to May 11 - 6 days. 

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
