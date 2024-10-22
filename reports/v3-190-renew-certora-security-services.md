# Proposal 190. Renew Certora as a Security Service Provider.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=190](https://vote.onaave.com/proposal/?proposalId=190)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-aave-certora-continuous-security-services/19262](https://governance.aave.com/t/arfc-aave-certora-continuous-security-services/19262)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x9cf002836453b464661F67841d61c24F1D830Bdb#code)

<br>

## Certora analysis

<br>

### Proposal types

:bank: payment stream

<br>

### Context

This proposal is the renewal of the security service provider - Certora for a duration of 365 days starting from the end of the previous engagement. The annual price for the project is $1.7M: $1.15M is paid in Gho vested linearly over one year, and $550,000 is paid in AAVE tokens vested linearly over one year.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xed54ffdae684c8085424c69e4792a1760a579cb9b32624c8391476dfcd0fd79b](https://etherscan.io/tx/0xed54ffdae684c8085424c69e4792a1760a579cb9b32624c8391476dfcd0fd79b)

```
- proposalId: 190
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x3d1fec3308264fb0c8fce54f95cd620d3b1d1578b5283f29935ef337069e3964
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
      "payloadId": "197" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x3d1fec3308264fb0c8fce54f95cd620d3b1d1578b5283f29935ef337069e3964" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/190.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/185.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/197.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/193.md)

<br>

### Technical analysis

We have verified that the payload creates a stream of 1.15M GHO and $550,000 worth of Aave for the duration specified for the address provided by Certora.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

