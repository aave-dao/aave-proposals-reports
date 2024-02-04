# V3. Proposal 14. Treasury management - GSM, RWA, Frontier budget preparation

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=14](https://vote.onaave.com/proposal/?proposalId=14)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-treasury-management-gsm-funding-rwa-strategy-preparations/16128](https://governance.aave.com/t/arfc-treasury-management-gsm-funding-rwa-strategy-preparations/16128)

<br>

## BGD analysis

<br>

### Proposal types

:bank: treasury

<br>

### Context

This proposal prepares funds in the Aave Ethereum Collector for the upcoming funding of the GSM (GHO Stability Module), RWA project with Centrifuge and Frontier staking as a service.
To do that, the majority of USD stablecoins are bridged from Polygon to Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x852847fcf90960c14e8dbe6f0916a712e1976efb6482bbbc6f3c666e6dd59b2c](https://etherscan.io/tx/0x852847fcf90960c14e8dbe6f0916a712e1976efb6482bbbc6f3c666e6dd59b2c)


```
- proposalId: 14
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x36664a88ec779d778e529d1175762ae8b062bcedc553c07936e158255ad31700
```

**createProposal() parameters**
```
{
  "payloads": [
    {
      "chain": "1",
      "accessLevel": 1,
      "payloadsController": "0xdabad81af85554e9ae636395611c58f7ec1aaec5",
      "payloadId": "52"
    },
    {
      "chain": "137",
      "accessLevel": 1,
      "payloadsController": "0x401b5d0294e23637c18fcc38b1bca814cda2637c",
      "payloadId": "30"
    }
  ],
  "votingPortal": "0x9b24c168d6a76b5459b1d47071a54962a4df36c3",
  "ipfsHash": "0x36664a88ec779d778e529d1175762ae8b062bcedc553c07936e158255ad31700"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/14.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/14.md)

**Payloads report**

**Ethereum**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/52.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/52.md)

<br>

**Polygon**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/30.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/30.md)

<br>

### Technical analysis

The proposal has 2 payloads, one in Ethereum and another in Polygon.

**[Ethereum](https://etherscan.io/address/0x7cAAf036c24e38eeA0688d2eD52A756Df83037fB#code#F1#L20)**

1. Withdraws ~128 ether to the Frontier Gnosis Safe, by redeeming them from Aave v2 Ethereum.
2. Sets the allowance of multiple Aave v2 aTokens to 0 on contracts used in the past for treasury management purposes.

<br>

**[Polygon](https://polygonscan.com/address/0x5E6ac2EEd9b13C4D093a281E78feda6bF4f6a8b5#code#F1#L22)**

This payload moves the majority of the Aave v2/v3 stablecoins held by the Aave Polygon Collector to the Ethereum Collector: all USDC and USDT, and all DAI from v2 but only 1'000'000 DAI from v3.

<br>

The proposal payload is consistent with the description in the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
