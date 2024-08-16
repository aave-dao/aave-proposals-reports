# Proposal 151. GHO Borrow Rate Update.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=151](https://vote.onaave.com/proposal/?proposalId=151)

<br>

### Governance forum discussion

[https://governance.aave.com/t/gho-stewards-adjustments-gho-borrow-rate/18649](https://governance.aave.com/t/gho-stewards-adjustments-gho-borrow-rate/18649)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x382C63705c18b5c354024f603ff7EFdcb492f8D6#code#F1#L28)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal decreases the borrow rate of the GHO token. BaseVariableBorrowRate of GHO is decreased to 6%.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xcdef94e5b68943fe7e8edc2d8893c69bd8174b16530c2028fb56530d01b56980](https://etherscan.io/tx/0xcdef94e5b68943fe7e8edc2d8893c69bd8174b16530c2028fb56530d01b56980)

```
- proposalId: 151
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x14648164c4d4c053dc982f0bcf4aed60ae802e0ec70b78afff085fe1075da455
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
      "payloadId": "162" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x14648164c4d4c053dc982f0bcf4aed60ae802e0ec70b78afff085fe1075da455" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/151.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/151.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/162.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/162.md)

<br>

### Technical analysis

We have verified that the payloads reduce the borrow rate of GHO to 6%.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
