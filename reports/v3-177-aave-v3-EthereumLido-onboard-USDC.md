# Proposal 177. Onboard USDC to Aave V3 Lido Instance

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=177](https://vote.onaave.com/proposal/?proposalId=177)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-onboard-usdc-to-aave-v3-lido-instance/19201](https://governance.aave.com/t/arfc-onboard-usdc-to-aave-v3-lido-instance/19201)

<br>

### Payloads

* EthereumLido - [proposal payloads](https://etherscan.io/address/0xd278BA5e3bDed95ebD0035b17662A9d02Cf1Ad09#code#F1#L28)

<br>

## Certora analysis

<br>

### Proposal types

:gem: :new: asset-listing

<br>

### Context

This proposal onboards USDC to the Aave v3 Lido Instance.
<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x8eb1c3210ffc31bd9be8deff674a7c901a4260ee644f1fa139d1bb191fd7f956](https://etherscan.io/tx/0x8eb1c3210ffc31bd9be8deff674a7c901a4260ee644f1fa139d1bb191fd7f956)

```
- proposalId: 177
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xdad5b7e0e98c8e85323902f8da177b99dd595302bebf9a69d40bbf0770072274
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
      "payloadId": "186" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xdad5b7e0e98c8e85323902f8da177b99dd595302bebf9a69d40bbf0770072274" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/177.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/177.md)

**Payload reports**

* EthereumLIdo - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/186.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/186.md)

<br>

### Technical analysis

We have verified that the payloads lists USDC on Lido Pool with the parameters mentioned in the IPFS.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

