# Proposal 16. AMPL Interest Rate Updates on V2 Ethereum

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=16](https://vote.onaave.com/proposal/?proposalId=16)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-ampl-interest-rate-updates-on-v2-ethereum/16189](https://governance.aave.com/t/arfc-ampl-interest-rate-updates-on-v2-ethereum/16189)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xE6175eBDFa6A53B6fbc1DB80955A8be73f03cFb1#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal updates AMPL interest rate parameter - slope2 and reserve factor parameter, on aave-v2 ethereum market as part of the deprecation plan. 

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x2e013fac6bc5b0795a50520dbea72e5049d93c4d59dcf2d5633145abca89c613](https://etherscan.io/tx/0x2e013fac6bc5b0795a50520dbea72e5049d93c4d59dcf2d5633145abca89c613)

```
- proposalId: 16
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x48d14f1fd7d5156c549cb107041da3d1329c05d95bbabba7d57eecbd8beedc45
```

<br>

**createProposal() parameters**

```
{
  "payloads": [
    {
      "chain": "1",
      "accessLevel": 1,
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
      "payloadId": "55"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0x48d14f1fd7d5156c549cb107041da3d1329c05d95bbabba7d57eecbd8beedc45"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/16.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/16.md)

**Payload reports**

* Ethereum V3 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/55.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/55.md)

<br>

### Technical analysis

We have verified that the payload modifies the slope2 and reserve factor of AMPL on the ethereum-v2 network to 0% and 99.9% respectively.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
