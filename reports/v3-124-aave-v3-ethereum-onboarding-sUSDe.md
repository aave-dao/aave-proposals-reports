# Proposal 119. Onboard sUSDe to Aave V3 on Ethereum

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=124](https://vote.onaave.com/proposal/?proposalId=124)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-onboard-susde-to-aave-v3-on-ethereum/17191/2](https://governance.aave.com/t/arfc-onboard-susde-to-aave-v3-on-ethereum/17191/2)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x1D76c5db48dC36381E16CDf17ac5936200474115#code)

<br>

## Certora analysis

<br>

### Proposal types

:gem: :new: asset-listing

<br>

### Context

This proposal onboards sUSDe onto Ethereum V3 in order to improve the diversity of assets on Aave and bolster liquidity within the ecosystem.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x2f2a58561e1c52e197e713ff0b969a26184528b4528d2c61fdd306eea8595848](https://etherscan.io/tx/0x2f2a58561e1c52e197e713ff0b969a26184528b4528d2c61fdd306eea8595848)

```
- proposalId: 124
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x7a9bcb55c0be36e9cd5c7d4122380aedbf5ea6834c9838770f81439a0a502283
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
      "payloadId": "140" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x7a9bcb55c0be36e9cd5c7d4122380aedbf5ea6834c9838770f81439a0a502283" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/124.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/124.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/140.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/140.md)

<br>

### Technical analysis

We have verified that the payload onboards sUSDe to Ethereum V3 with the same configuration declared in the IPFS.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
