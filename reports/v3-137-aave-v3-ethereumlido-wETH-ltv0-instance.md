# Proposal 137. wETH LTV0 Aave V3 Lido Instance.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=137](https://vote.onaave.com/proposal/?proposalId=137)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-deploy-a-lido-aave-v3-instance/18047/18](https://governance.aave.com/t/arfc-deploy-a-lido-aave-v3-instance/18047/18)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x216fAe9De67299D7792890b51F5aB7F37cDc62c1#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal sets the LTV of wETH on ethereumLido market to 0 in order to shift focus to the instance's intended main use case of leveraged staking.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x7c7ddea817919adb509faa6bf0f5b38f1618e0d033140ea4f9fbfcb41f02a363](https://etherscan.io/tx/0x7c7ddea817919adb509faa6bf0f5b38f1618e0d033140ea4f9fbfcb41f02a363)

```
- proposalId: 137
- creator: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- accessLevel: 1
- ipfsHash: 0x39d3766a07eaacdbbd38e2b759e37f02ff453180574b52efcaa25334c42177ee
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
      "payloadId": "151"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0x39d3766a07eaacdbbd38e2b759e37f02ff453180574b52efcaa25334c42177ee"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/137.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/137.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/151.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/151.md)

<br>

### Technical analysis

We have verified that the payload modifies the LTV of wETH on EthereumLido to 0.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

