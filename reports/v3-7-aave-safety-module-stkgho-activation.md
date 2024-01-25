# V3. Proposal 7. Aave Safety Module - stkGHO activation

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=7](https://vote.onaave.com/proposal/?proposalId=7)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-upgrade-safety-module-with-stkgho/15635](https://governance.aave.com/t/arfc-upgrade-safety-module-with-stkgho/15635)

<br>

## BGD analysis

<br>

### Proposal types

safety-module

<br>

### Context

This proposal activates stkGHO, a new instance of the Aave Safety Module, by configuring an emission of AAVE rewards for stakers.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xebf44760daa0681e22117904260e1c40ba3f5792b472ded64d7ddaeb4bca9c04](https://etherscan.io/tx/0xebf44760daa0681e22117904260e1c40ba3f5792b472ded64d7ddaeb4bca9c04)


```
- proposalId: 7
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xbaf47f585bee303606be09f9f9c4215875e8ab48df280c5cabebb94d722a5dd2
```

**createProposal() parameters**
```
{
  "payloads": [
    {
      "chain": "1",
      "accessLevel": 1,
      "payloadsController": "0xdabad81af85554e9ae636395611c58f7ec1aaec5",
      "payloadId": "47"
    }
  ],
  "votingPortal": "0x9b24c168d6a76b5459b1d47071a54962a4df36c3",
  "ipfsHash": "0xbaf47f585bee303606be09f9f9c4215875e8ab48df280c5cabebb94d722a5dd2"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/7.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/7.md)

**Payloads report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/47.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/47.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xc66A72836B7832372A799b5E564dFa8Ed10df405#code#F1#L16) does the following:

1. Configure emission of AAVE tokens on [stkGHO](https://etherscan.io/address/0x1a88Df1cFe15Af22B3c4c783D4e6F7F9e0C1885d) with the following parameters:
  - **Emission**: 50 AAVE per day (in emission per second).
  - **Distribution end**: 90 days from proposal execution.
2. Approve ~4'500 AAVE from the Aave Ecosystem Reserve to stkGHO, to allow claming of them by stakers.

<br>

The proposal payload is consistent with the description in the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
