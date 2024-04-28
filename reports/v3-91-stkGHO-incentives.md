# Proposal 91. stkGHO Incentives.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=91](https://vote.onaave.com/proposal/?proposalId=91)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-amend-safety-module-emissions/16640](https://governance.aave.com/t/arfc-amend-safety-module-emissions/16640)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xe30Ef3C5acac776b5e0aC6E7E103f9B5f81e06Ae#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal enables stkGHO incentives emissions for 180 days with 100 AAVE per day, after the previous period ended, in order to support GHO peg and to pave the way for future GHO supply expansion.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x39ccd1b211dd2f5ad8e14da6bf5e714dfe3255cf9a374750e0a67927d0fcfdb9](https://etherscan.io/tx/0x39ccd1b211dd2f5ad8e14da6bf5e714dfe3255cf9a374750e0a67927d0fcfdb9)

```
- proposalId: 91
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x633733ef9b80afd497fd1a25d848fbe91ef694fab798dbbc27617ca07407454c
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
      "payloadId": "115" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x633733ef9b80afd497fd1a25d848fbe91ef694fab798dbbc27617ca07407454c" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/91.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/91.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/115.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/115.md)

<br>

### Technical analysis

We have verified that the payload is executing the following actions:

1. Set new allowance to STK_GHO of 100 AAVE per day for 180 days

2. Set distribution end for 180 days from Execution date

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
