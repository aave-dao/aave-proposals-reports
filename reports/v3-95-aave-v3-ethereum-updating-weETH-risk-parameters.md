# Proposal 95. Updating weETH Risk Parameters.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=95](https://vote.onaave.com/proposal/?proposalId=95)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-updating-weeth-risk-parameters/17402](https://governance.aave.com/t/arfc-updating-weeth-risk-parameters/17402)

<br>

### Payloads

* Ethereum V3- [proposal payloads](https://etherscan.io/address/0x59C6F019a5ee207d5b719D690bfDd287e7FaFCf0#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal modifies weETH risk parameters on Ethereum v3 in order to increase Aave DAO revenue and encourage collateral adoption.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x7adb7f075a52dbcc8b3c642d646781b8debf898440fb6fb226d339f07edba1bf](https://etherscan.io/tx/0x7adb7f075a52dbcc8b3c642d646781b8debf898440fb6fb226d339f07edba1bf)

```
- proposalId: 95
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xc486b689997f162ab5616ffb614eaffde14c8787bb06298b8100d3718267b255
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
      "payloadId": "118" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xc486b689997f162ab5616ffb614eaffde14c8787bb06298b8100d3718267b255" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/95.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/95.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/118.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/118.md)

<br>

### Technical analysis

We have verified that the payload modifies the following risk parameters of weETH on Ethereum v3:

    Supply Cap: 84,000

    Borrows Cap: 29,500

    Uoptimal: 35%

    reserve factor: 45%

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
