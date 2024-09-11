# Proposal 162. Orbit Program Renewal - Q3 2024.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=162](https://vote.onaave.com/proposal/?proposalId=162)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-orbit-program-renewal-q3-2024/18834](https://governance.aave.com/t/arfc-orbit-program-renewal-q3-2024/18834)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x8d85e42BB8dE496ef63D28C58b54b1d9580d8564#code#F1#L1) 


<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal is the renewal of the Orbit program for recognized delegates, compensating them with GHO and ETH reimbursement of Gas costs , associated with their governance activity.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xb4d985df697527008febdc395b2533e73e47e214508a114ec35d3bb8027ca81e](https://etherscan.io/tx/0xb4d985df697527008febdc395b2533e73e47e214508a114ec35d3bb8027ca81e)

```
- proposalId: 162
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xc272f529dc38017c4880f8af0ec5fc13ca3f6c5de9be35e457ff5862fce1183c
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
      "payloadId": "170" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xc272f529dc38017c4880f8af0ec5fc13ca3f6c5de9be35e457ff5862fce1183c" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/162.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/162.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/170.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/170.md)



<br>

### Technical analysis

We have verified that the payload executes the following financial actions:

- Transfer 2200 GHO (a one-off compensation worth 13 days of stream) to the provided addresses by EzR3al, StableNode, Saucy Block, Areta.

- Create a stream of 15,000 GHO of 90 days to the provided addresses by EzR3al, StableNode, Saucy Block, Areta.

- Transfer 2.91 ETH to ACI, 0.67 ETH to Catapulta and 0.72 ETH to TokenLogic as gas rebate.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum except for the 2200 GHO compensation.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
