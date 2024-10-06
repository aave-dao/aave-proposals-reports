# Proposal 179. Aave Liquidity Committee Funding Pary IV.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=179](https://vote.onaave.com/proposal/?proposalId=179)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-aave-liquidity-committee-funding-phase-iv/19188](https://governance.aave.com/t/arfc-aave-liquidity-committee-funding-phase-iv/19188)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x9Ed119F4e1966B4a7e6be384D6b42BB6da9f981a#code#F1#L13)

<br>

## Certora analysis

<br>

### Proposal types

:moneybag: :receipt: asset transfer

<br>

### Context

This proposal funds the Aave Liquidity Committee (ALC) with 950k GHO to enhance GHO liquidity on Ethereum and Arbitrum through integrations with various protocols, sustaining liquidity pools, and driving broader adoption of GHO across decentralized finance (DeFi) ecosystems.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xad7b5f9b4e882c89e84302b9413f9fc0126012a6465ac03cd1e6f63f6f8e29ef](https://etherscan.io/tx/0xad7b5f9b4e882c89e84302b9413f9fc0126012a6465ac03cd1e6f63f6f8e29ef)

```
- proposalId: 179
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x533f3e36e9407910de9501e672099ca132cf37410ac6f475f940b2c0536687aa
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
      "payloadId": "187" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x533f3e36e9407910de9501e672099ca132cf37410ac6f475f940b2c0536687aa" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/179.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/179.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/187.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/187.md)

<br>

### Technical analysis

We have verified that an allowance of 950k GHO has been approved from the Aave Treasury to the Aave Liquidity Committee (ALC) SAFE wallet on Ethereum (0xA1c93D2687f7014Aaf588c764E3Ce80aF016229b).

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
