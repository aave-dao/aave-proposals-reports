# Proposal 52. Aave Liquidity Committee Funding.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=52](https://vote.onaave.com/proposal/?proposalId=52)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-aave-liquidity-committee-funding/16793](https://governance.aave.com/t/arfc-aave-liquidity-committee-funding/16793)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x27DD6e442FE3B1c625B50Dc338a59005d5EA4354#code#F1#L91)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal funds the Aave Liquidity Committee (ALC) with 500k GHO to further stabilize USD peg and establish its utility through integration with variety of DeFi protocols.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x584aec551283b86eb809992f392043f57259eb6c193718a78647a99c5607a94b](https://etherscan.io/tx/0x584aec551283b86eb809992f392043f57259eb6c193718a78647a99c5607a94b)

```
- proposalId: 52
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x488049214c45263bdb7a736cb12a857d7e6f269ad6df8f76bf18361ea25ec921
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
      "payloadId": "82" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x488049214c45263bdb7a736cb12a857d7e6f269ad6df8f76bf18361ea25ec921" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/52.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/52.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/82.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/82.md)

<br>

### Technical analysis

We have verified that the following aTokens were withdrawn from the Aave V2 pool on behalf of the treasury and swapped to gho:

USDC: 250k

USDT: 250k

We also verified that 500k GHO were approved as allowance to the ALC SAFE wallet from the treasury.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
