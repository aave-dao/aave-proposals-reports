# V3. Proposal 16. Aave v2 Ethereum - Rate strategy update

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=16](https://vote.onaave.com/proposal/?proposalId=16)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-ampl-interest-rate-updates-on-v2-ethereum/16189](https://governance.aave.com/t/arfc-ampl-interest-rate-updates-on-v2-ethereum/16189)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal changes Slope 2 on the AMPL interest rate strategy on Aave v2, in order to contain the virtual "growth" of aToken.
Additionally, it also increase the RF of the asset to 99.9%.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x2e013fac6bc5b0795a50520dbea72e5049d93c4d59dcf2d5633145abca89c613](https://etherscan.io/tx/0x2e013fac6bc5b0795a50520dbea72e5049d93c4d59dcf2d5633145abca89c613)


```
- proposalId: 16
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x48d14f1fd7d5156c549cb107041da3d1329c05d95bbabba7d57eecbd8beedc45
```

**createProposal() parameters**
```
{
  "payloads": [
    {
      "chain": "1",
      "accessLevel": 1,
      "payloadsController": "0xdabad81af85554e9ae636395611c58f7ec1aaec5",
      "payloadId": "55"
    }
  ],
  "votingPortal": "0x9b24c168d6a76b5459b1d47071a54962a4df36c3",
  "ipfsHash": "0x48d14f1fd7d5156c549cb107041da3d1329c05d95bbabba7d57eecbd8beedc45"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/16.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/16.md)

**Payloads report**

**Ethereum**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/55.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/55.md)

<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xE6175eBDFa6A53B6fbc1DB80955A8be73f03cFb1#code#F1#L17) does the following changes on AMPL:

- Rate Slope 2: 300% -> **0%**
- RF: 99% -> **99.9%**

<br>

The proposal payload is consistent with the description in the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
