# Proposal 96. Polygon V2 Reserve Factor Updates & Interest Rate Increases.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=96](https://vote.onaave.com/proposal/?proposalId=96)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-polygon-v2-borrow-rate-adjustments/17252](https://governance.aave.com/t/arfc-polygon-v2-borrow-rate-adjustments/17252)

[https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937/22](https://governance.aave.com/t/arfc-reserve-factor-updates-polygon-aave-v2/13937/22)

<br>

### Payloads

* Polygon V2- [proposal payloads](https://polygonscan.com/address/0x0a8EE19Cbd27Bd2F39C53623E8fC95778cBfB904#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal increases the reserve factors and also revises the Borrow Rate of multiple assets on Aave-V2-Polygon by 5% up to 99.99% in order to encouraging users to migrate from Polygon v2 to v3.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x08dd6a35af5838fedb7316bda9dbcc112ee3400da7187b9b81a3bba035ede60b](https://etherscan.io/tx/0x08dd6a35af5838fedb7316bda9dbcc112ee3400da7187b9b81a3bba035ede60b)

```
- proposalId: 96
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xcd04c72e36d8208c2ade9752e9ffded55acde06b1d8152391721eb1b1ba1406c
```

<br>

**createProposal() parameters**

```
{
  "payloads": [ 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "60" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xcd04c72e36d8208c2ade9752e9ffded55acde06b1d8152391721eb1b1ba1406c" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/96.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/96.md)

**Payload reports**

* Polygon - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/60.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/60.md)

<br>

### Technical analysis

We have verified that the payload modifies the reserve factor of the following tokens to the following values:

    USDC: 98%

    USDT: 97%

    DAI: 96%

We have also verified that the payload modifies the variable slopes and Uoptimal of the following tokens to the following values:

- BAL:

    slope1: 50%

    slope2: 134%

    Uoptimal: 20%

- CRV:

    slope1: 50%

    slope2: 134%

    Uoptimal: 10%

- DAI:

    slope1: 9.75%

    slope2: 134%

    Uoptimal: 71%

- GHST:

    slope1: 50%

    slope2: 134%

    Uoptimal: 10%

- LINK:

    slope1: 50%

    slope2: 134%

    Uoptimal: 10%

- USDT:

    slope1: 9.75%

    slope2: 134%

    Uoptimal: 52%

- wBTC:

    slope1: 4.75%

    slope2: 134%

    Uoptimal: 37%

- wETH:

    slope1: 4.75%

    slope2: 134%

    Uoptimal: 40%

- wMATIC:

    slope1: 6.75%

    slope2: 134%

    Uoptimal: 48%

- USDC:

    slope1: 9.75%

    slope2: 134%

    Uoptimal: 77%

<br>

The proposal is consistent with the description on both Snapshot and the governance forum except the value of slope1 on DAI, USDC, USDT which is changed from 9% to 9.75%.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
