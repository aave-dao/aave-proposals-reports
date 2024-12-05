# Proposal 213. Remove Frax from Isolation Mode.


<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=213](https://vote.onaave.com/proposal/?proposalId=213)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-remove-frax-from-isolation-mode-on-aave-v3-mainnet/19337](https://governance.aave.com/t/arfc-remove-frax-from-isolation-mode-on-aave-v3-mainnet/19337)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xb8F4dF0aE61E6dE45877c01eE73d7192Bb15028C#code)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal suggests removing FRAX from isolation mode to facilitate further AMO deployments.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x4bbcd8cb66d5292e04e9c0d013ce46c4ca66851052a3b247d1a6346c98459e5e](https://etherscan.io/tx/0x4bbcd8cb66d5292e04e9c0d013ce46c4ca66851052a3b247d1a6346c98459e5e)

```
- proposalId: 213
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x141a3189c70b282415870d2c3ea6f7c05d256c8033b41895293ae74989c2b1b9
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
      "payloadId": "217" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x141a3189c70b282415870d2c3ea6f7c05d256c8033b41895293ae74989c2b1b9" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/213.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/213.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/217.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/217.md)


<br>

### Technical analysis

The technical analysis confirms that the debt ceiling parameter for FRAX is set to 0, ensuring no additional borrowing is possible. Additionally, the isolationModeTotalDebt parameter has been updated to 0, reflecting the removal of FRAX from Isolation Mode and ensuring it no longer contributes to the total debt calculation in this mode.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

