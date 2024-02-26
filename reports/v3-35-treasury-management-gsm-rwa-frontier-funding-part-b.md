# Proposal 35. Treasury Management - GSM Funding & RWA Strategy Preparations (Part 2)

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=35](https://vote.onaave.com/proposal/?proposalId=35)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-treasury-management-gsm-funding-rwa-strategy-preparations/16128](https://governance.aave.com/t/arfc-treasury-management-gsm-funding-rwa-strategy-preparations/16128)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xC8dFf20e4141F52A1d8731642212E9d8253b7dF5#code#F1#L32)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal swaps funds from treasury and deposit them in the collector in order to prepare for the GSM and RWA funding.
To do that, 0.7M USDC, and all DAI are swapped to USDT and deposited to the pool.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x3b7463c9b2c59fad2dead24f4c84e07af7353203e7558a3050af49e4c2d108db](https://etherscan.io/tx/0x3b7463c9b2c59fad2dead24f4c84e07af7353203e7558a3050af49e4c2d108db)

```
- proposalId: 35
- creator: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- accessLevel: 1
- ipfsHash: 0x9206b8d1ee912b328fccf81311e1b20ddff390d2351d6be27dadaa230584c29f
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
      "payloadId": "65" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x9206b8d1ee912b328fccf81311e1b20ddff390d2351d6be27dadaa230584c29f" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/35.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/35.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/65.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/65.md)

<br>

### Technical analysis

We have verified that the payload:

1. Swaps 0.7 USDC and all the DAI in the collector into USDT via the Aave swapper.
2. Deposits all the rest of the USDC in the collector to the V3 pool.
3. Enables deposit of all the swapped USDT to the V3 pool in a later time when the swap query is fulfilled.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
