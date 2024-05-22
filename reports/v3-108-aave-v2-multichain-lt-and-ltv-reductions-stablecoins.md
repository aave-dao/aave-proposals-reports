# Proposal 108. LT/LTV Reductions on Aave V2 Stablecoins.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=108](https://vote.onaave.com/proposal/?proposalId=108)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-lt-ltv-reductions-on-aave-v2-stablecoins/17508](https://governance.aave.com/t/arfc-lt-ltv-reductions-on-aave-v2-stablecoins/17508)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x1e0cd108bFdE3fcC5e90A862De8F88c1e09eb939#code#F1#L1)

* Polygon - [proposal payloads](https://polygonscan.com/address/0xA0C047D831fEEb599d2196AdDb3e84D5C59F7C86#code#F1#L1)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x51b1fa548ca9B09Dd6cdbf428aca522B72ef8439/contract/43114/code)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal reduces the LT and LTV of major stable-coins on Aave-V2-Ethereum, Aave-V2-Polygon and Aave-V2-Avalanche in order to limit risks posed by the current parameters and align them closer to V3’s parameters.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x8f5ac2578ad04482f9b60110c3a4b868f77b93acca2cf224b4af8860105c5771](https://etherscan.io/tx/0x8f5ac2578ad04482f9b60110c3a4b868f77b93acca2cf224b4af8860105c5771)

```
- proposalId: 108
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xb34fab83149275adabf38be78dbf8f3def00751702a77efd9f6e1fdc901e8358
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
      "payloadId": "129" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "64" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "34" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xb34fab83149275adabf38be78dbf8f3def00751702a77efd9f6e1fdc901e8358" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/108.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/108.md)

**Payload reports**

* Ethereum V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/129.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/129.md)

* Polygon V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/64.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/64.md)

* Avalanche V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/34.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/34.md)

<br>

### Technical analysis

We have verified that the payload reduces the LTs and LTVs of the following tokens to the following values:

- Ethereum V2:

    USDC:

        LTV: 75%

        LT: No Change

- Polygon V2:

    USDC:

        LTV: 75%

        LT: 84.5%

- Avalanche V2:

    USDC:

        LTV: No Change

        LT: 78%

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
