# Proposal 75. Interim aAMPL Distribution.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=75](https://vote.onaave.com/proposal/?proposalId=75)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-aampl-interim-distribution/17184](https://governance.aave.com/t/arfc-aampl-interim-distribution/17184)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x65a4523f05b0443A3f4fdeA30CB7759AB816241B#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal is an interim distribution of 298,543.52244 USDC to allow aAMPL suppliers to proceed partially with their withdrawals after a problem was detected on the AMPL custom reserve on Aave v2 Ethereum, causing an unexpected inflation of AMPL-related balances and supply.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x536d9bdd739379e6bc3ca22e1456d905aaddf9a811e1269d7e772eab3a12b046](https://etherscan.io/tx/0x536d9bdd739379e6bc3ca22e1456d905aaddf9a811e1269d7e772eab3a12b046)

```
- proposalId: 75
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0x33032b8a57db207e3f6ba5a964f6a438ef6e9a17219ba93b0a51b3ddc69e5ca5
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
      "payloadId": "102" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x33032b8a57db207e3f6ba5a964f6a438ef6e9a17219ba93b0a51b3ddc69e5ca5" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/75.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/75.md)

**Payload reports**

* Ethereum V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/102.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/102.md)

<br>

### Technical analysis

We have verified that the payload is executing the following actions:

1. Withdraw 298,543.522440 USDC from the collector.

2. Approve the full amount to 0x8BB4C975Ff3c250e0ceEA271728547f3802B36Fd which is the distribution creator by Angle Labs.

3. Sign the tos of https://app.merkl.xyz/ via a onchain transaction.

4. Create a campaign to distribute funds to the affected users with the following parameters:

    rewardToken: USDC.

    amount: 297,050.804827.

    startTimestamp: 2 hours after the execution of the payload.

    duration: 1 hour.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
