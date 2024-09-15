# Proposal 164. wstETH Borrow Cap Reduction.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=164](https://vote.onaave.com/proposal/?proposalId=164)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-lido-instance-reduce-wsteth-borrow-cap/19016](https://governance.aave.com/t/arfc-lido-instance-reduce-wsteth-borrow-cap/19016)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x60B778EEC3433Aaa8f1C08A904227048e243ce8c#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal decreases wstETH borrow-cap from 12,000 to 100 on Aave-V3-EthereumLido in preparation for wstETH deposit incentives.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x1afbb368e2ed70b1a819495e93c072db95a3bd9b6e867cd6f8279e0376548745](https://etherscan.io/tx/0x1afbb368e2ed70b1a819495e93c072db95a3bd9b6e867cd6f8279e0376548745)

```
- proposalId: 164
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xb3c587d4f09e9f879cf2b793b127c927522a4cb3eeb04623241916ea9ff5dae5
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
      "payloadId": "172" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xb3c587d4f09e9f879cf2b793b127c927522a4cb3eeb04623241916ea9ff5dae5" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/164.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/164.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/172.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/172.md)

<br>

### Technical analysis

We have verified that the payload decreases wstETH borrow-cap on Aave-V3-EthereumLido from 12,000 wstETH to 100 wstETH.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
