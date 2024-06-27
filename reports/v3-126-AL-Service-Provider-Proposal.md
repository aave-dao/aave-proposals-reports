# Proposal 126. AL Service Provider Proposal

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=126](https://vote.onaave.com/proposal/?proposalId=126)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-al-service-provider-proposal/17974](https://governance.aave.com/t/arfc-al-service-provider-proposal/17974)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x14eEe3F95752404C35e1c7fE7f03A39431edb272#code)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

:bank: payment stream

<br>

### Context

This AIP proposes a one-year technical contributor engagement for the Aave Labs to act as a service provider for development of Aave V4 and a new visual identity.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xaa9b52afa821bd948aae29a5379c4720e162f9728c6a81bcd488f877bd213615](https://etherscan.io/tx/0xaa9b52afa821bd948aae29a5379c4720e162f9728c6a81bcd488f877bd213615)

```
- proposalId: 126
- creator: 0x66a28531e6f390a8cd44ab0c57a0f1aeb7e673ff
- accessLevel: 1
- ipfsHash: 0x344e41de99f056c9ab5e6b78f0bb4c25b6332c49c4e4c645c71c4af2a425c29d
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
      "payloadId": "141" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x344e41de99f056c9ab5e6b78f0bb4c25b6332c49c4e4c645c71c4af2a425c29d" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/126.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/126.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/141.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/141.md)

<br>

### Technical analysis

We have verified that the payload executes the following actions:

- create payment stream of 9,000,000 GHO spanning a duration of 365 days to the address 0x1c037b3C22240048807cC9d7111be5d455F640bd

- transfer a sum of 3,000,000 GHO to to the address 0x1c037b3C22240048807cC9d7111be5d455F640bd


<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
