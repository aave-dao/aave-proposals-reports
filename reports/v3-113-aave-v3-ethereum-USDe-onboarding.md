# Proposal 113. Onboard USDe Aave V3 Ethereum.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=113](https://vote.onaave.com/proposal/?proposalId=113)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-onboard-usde-to-aave-v3-on-ethereum/17690](https://governance.aave.com/t/arfc-onboard-usde-to-aave-v3-on-ethereum/17690)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x22e4d16763F70c89E210F07dCFEd9219298Dc72d#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:gem: :new: asset-listing

<br>

### Context

This proposal onboards USDe onto Ethereum V3, eyeing the future for sUSDe which has high potential for borrowing demand. 

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x5fcaf50d9e7168edb04e62d0b51fe66c9e823f1ac4671b4fe47969912b203dc7](https://etherscan.io/tx/0x5fcaf50d9e7168edb04e62d0b51fe66c9e823f1ac4671b4fe47969912b203dc7)

```
- proposalId: 113
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x08e45bba0b43b052d9a0f7fe683addee20c3ce9100979540f8b24e10a74ce869
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
      "payloadId": "133" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x08e45bba0b43b052d9a0f7fe683addee20c3ce9100979540f8b24e10a74ce869" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/113.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/113.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/133.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/133.md)

<br>

### Technical analysis

We have verified that the payload onboards USDe to Ethereum V3 with the same configuration declared in the IPFS.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
