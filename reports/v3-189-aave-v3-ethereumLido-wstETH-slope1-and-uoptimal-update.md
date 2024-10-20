# Proposal 189. wstETH Slope1 &amp; Uoptimal Update.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=189](https://vote.onaave.com/proposal/?proposalId=189)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-lido-instance-wsteth-slope1-uoptimal-update/19069](https://governance.aave.com/t/arfc-lido-instance-wsteth-slope1-uoptimal-update/19069)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x0c8eD72f00ABAA98D4E980e4f4c3464ce8d6737b#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal adjusts the Uoptimal and variable slope1 of wstETH on the ethereumLido market to 80% and 2.25% respectively in order to improve the capital efficiency of the asset on the market.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x9af9a606cb38f3c2fad7c9cc85a446a1cc000f0ac71546bdd1d756f000c9f7f3](https://etherscan.io/tx/0x9af9a606cb38f3c2fad7c9cc85a446a1cc000f0ac71546bdd1d756f000c9f7f3)

```
- proposalId: 189
- creator: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- accessLevel: 1
- ipfsHash: 0x3a149264a56d0860bce568f8f75e4054bf24bfcbd73dc0d663bb0662528162ca
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
      "payloadId": "196"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0x3a149264a56d0860bce568f8f75e4054bf24bfcbd73dc0d663bb0662528162ca"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/189.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/189.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/196.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/196.md)

<br>

### Technical analysis

We have verified that the payload modifies the following parameters of wstETH on the ethereumLido market:

- Uoptimal: From: 45%  To: 80%

- variable slope1: From: 3.5%  To: 2.25%

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

