# Proposal 81. Ethereum V2 LT Reductions.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=81](https://vote.onaave.com/proposal/?proposalId=81)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-ethereum-v2-lt-reductions-04-15-2024/17369](https://governance.aave.com/t/arfc-chaos-labs-ethereum-v2-lt-reductions-04-15-2024/17369)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x3e7b6298a8Ff538338d361D2976D0EB196635097#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal reduces liquidation thresholds of multiple assets on Aave-V2-Ethereum as part of the v2 deprecation.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x9dc1db64b508c3038ae129215bfcae507ca92a6cc71ac67cb598f8186da0ef08](https://etherscan.io/tx/0x9dc1db64b508c3038ae129215bfcae507ca92a6cc71ac67cb598f8186da0ef08)

```
- proposalId: 81
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xf76a0f5f4db1f1718f9f0bc3116895eaa92b61020af1fc5059f27ee16f390500
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
      "payloadId": "108" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xf76a0f5f4db1f1718f9f0bc3116895eaa92b61020af1fc5059f27ee16f390500" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/81.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/81.md)

**Payload reports**

* Ethereum V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/108.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/108.md)


<br>

### Technical analysis

We have verified that the payload reduces the liquidation thresholds of the following tokens:

    CRV: 0.01%

    LINK: 68%

    MKR: 10%

    UNI: 0.01%

    ZRX: 5%

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
