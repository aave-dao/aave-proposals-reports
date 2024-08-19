# Proposal 152. enabling Metis token as collateral on Aave V3.
<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=152](https://vote.onaave.com/proposal/?proposalId=152)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-enable-metis-as-collateral-on-metis-chain/16658](https://governance.aave.com/t/arfc-enable-metis-as-collateral-on-metis-chain/16658)

<br>

### Payloads

* Metis - [proposal payloads](https://explorer.metis.io/address/0x0eC1A3d247843b688b354BFF80444B952a08C663/contract/1088/code#loaded)

<br>

## Certora analysis

<br>

### Proposal types

:gem: :new: asset-listing

<br>

### Context

This proposal enables Metis token as collateral on Aave V3 withing the Metis Chain.

<br>

### Proposal creation

Transaction: [https://explorer.metis.io/tx/0x4ff18f8f61801948a1a1b383d9c653ea3e4189b747e756b42c4459153a1da3d1](https://explorer.metis.io/tx/0x4ff18f8f61801948a1a1b383d9c653ea3e4189b747e756b42c4459153a1da3d1)

```
- proposalId: 152
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xcdd44ece79347739c5bd2c69e16f9ddd462f073aa4e0533342a3a3ec7c71d136
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "1088", 
      "accessLevel": "1", 
      "payloadsController": "0x2233F8A66A728FBa6E1dC95570B25360D07D5524", 
      "payloadId": "23" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xcdd44ece79347739c5bd2c69e16f9ddd462f073aa4e0533342a3a3ec7c71d136" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/152.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/152.md)

**Payload reports**

* Metis - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/23_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/23_forge.md)

<br>

### Technical analysis

We have verified that the payload setting up the parameters correctly to the Metis token. The Debt Ceiling configuration in the `preExecute()` function is intended to avoid a revert because of the LT is initialy set up to 0 .

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
