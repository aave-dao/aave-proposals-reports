# Proposal 57. Ethereum v2 Reserve Factor Adjustment.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=57](https://vote.onaave.com/proposal/?proposalId=57)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-ethereum-v2-reserve-factor-adjustment/16764/3](https://governance.aave.com/t/arfc-ethereum-v2-reserve-factor-adjustment/16764/3)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xA26adC887e62C414553cCc821B91a8027f1d12aa#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal increases the reserve factors of multiple assets on Aave-V2-Ethereum by 5% up to 99.99% in order to encouraging users to migrate from Ethereum v2 to v3.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x6a0daf39d74206e35f7a6a002756a78d1ede5575306a29332eb7330907b7e2c9](https://etherscan.io/tx/0x6a0daf39d74206e35f7a6a002756a78d1ede5575306a29332eb7330907b7e2c9)

```
- proposalId: 57
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x2fce141813b52ab4fc26fe0bc35cc4d219acd0985582aa993813b66515b7ae16
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
      "payloadId": "86" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x2fce141813b52ab4fc26fe0bc35cc4d219acd0985582aa993813b66515b7ae16" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/57.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/57.md)

**Payload reports**

* Ethereum V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/86.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/86.md)

<br>

### Technical analysis

We have verified that the payload modifies the reserve factor of the following tokens to the following values:

DAI: 35.00%

FRAX: 40.00%

GUSD: 30.00%

LINK: 40.00%

LUSD: 35.00%

sUSD: 40.00%

USDC: 35.00%

USDP: 30.00%

USDT: 35.00%

WBTC: 40.00%

WETH: 35.00%

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
