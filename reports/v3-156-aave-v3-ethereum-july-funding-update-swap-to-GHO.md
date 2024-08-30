# Proposal 156. Aave V3 Ethereum funding of the Merit and Ahab programs swapping stablecoins in treasury to GHO.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=156](https://vote.onaave.com/proposal/?proposalId=156)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-july-funding-update/18447](https://governance.aave.com/t/arfc-july-funding-update/18447)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xfc8aC585146F1bf84e77E582A202AC5e58eFC94b#code#F1#L1) 


<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal will swap assets held in the Treasury for GHO and fund Phase III of the Merit and Ahab programs.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x40cd88631889d5c209fa6963a2e9426b11e6f0b3842b261ca5548cbe94587160](https://etherscan.io/tx/0x40cd88631889d5c209fa6963a2e9426b11e6f0b3842b261ca5548cbe94587160)

```
- proposalId: 156
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xd46124e556c224e5e9a5b4d202548931ea58f9dee5bb517929166ce0f068813c
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
      "payloadId": "164" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xd46124e556c224e5e9a5b4d202548931ea58f9dee5bb517929166ce0f068813c" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/156.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/156.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/164.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/164.md)



<br>

### Technical analysis

We have verified the underlying and price feed addresses are correct, the swapping mechanism done properly and the amounts swapped and transfered are inline with the both Snapshot and the governance forum.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
