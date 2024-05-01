# Proposal 93. aAMPL Second Distribution.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=93](https://vote.onaave.com/proposal/?proposalId=93)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-aampl-second-distribution/17464](https://governance.aave.com/t/arfc-aampl-second-distribution/17464)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xeD5e9711D93C09c91cd61ec6e3ddBcD58A9e963D#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal is the second distribution of 762,604.60971 aUSDC to allow aAMPL suppliers to proceed partially with their withdrawals after a problem was detected on the AMPL custom reserve on Aave v2 Ethereum, causing an unexpected inflation of AMPL-related balances and supply. This is a follow up of AIP 75 which distributed 300,000$.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x2c54da9b6a95305e5a824a35c310b8e3444bd62412b7d086cda51bd4b8b0cb37](https://etherscan.io/tx/0x2c54da9b6a95305e5a824a35c310b8e3444bd62412b7d086cda51bd4b8b0cb37)

```
- proposalId: 93
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0x0d7d6e71a610c1f6373cb8e8fb09b7a8f2741bf0264f1175358b1b1ec0062839
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
      "payloadId": "116" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x0d7d6e71a610c1f6373cb8e8fb09b7a8f2741bf0264f1175358b1b1ec0062839" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/93.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/93.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/116.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/116.md)

<br>

### Technical analysis

We have verified that the payload is executing the following actions:

1. Transfer 766,436.793679 aUSDC from the collector.

2. Approve the full amount to 0x8BB4C975Ff3c250e0ceEA271728547f3802B36Fd which is the distribution creator by Angle Labs.

3. Create a campaign to distribute funds to the affected users with the following parameters:

    rewardToken: aUSDC.

    amount: 762,604.609710.

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
