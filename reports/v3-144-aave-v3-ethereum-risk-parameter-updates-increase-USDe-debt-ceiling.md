# Proposal 144. Risk Parameter Updates - Increase USDe Debt Ceiling on V3 Ethereum.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=144](https://vote.onaave.com/proposal/?proposalId=144)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-increase-usde-debt-ceiling-on-v3-ethereum-07-22-2024/18325](https://governance.aave.com/t/arfc-chaos-labs-risk-parameter-updates-increase-usde-debt-ceiling-on-v3-ethereum-07-22-2024/18325)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x95a4cd8f9F86e0FDAc73648bA654c2f04F1c3090#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal increases debt ceiling of USDe on Ethereum-V3 market following rapid deposits and borrows against these deposits on Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x4d2b6b81036149898bff09247229a4c4e43bc9ca12cd5e29b4e0f47bea53c886](https://etherscan.io/tx/0x4d2b6b81036149898bff09247229a4c4e43bc9ca12cd5e29b4e0f47bea53c886)

```
- proposalId: 144
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x3c38f5d5c0f5098b71caed9f45dd54ec34483bb66faea52736e79f445b9a96af
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
      "payloadId": "156" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x3c38f5d5c0f5098b71caed9f45dd54ec34483bb66faea52736e79f445b9a96af" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/144.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/144.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/152.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/156.md)

<br>

### Technical analysis

We have verified that the payload increases the debt ceiling of USDe on Ethereum-V3 market from 40M to 50M.

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

