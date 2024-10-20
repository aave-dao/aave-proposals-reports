# Proposal 188. Reserve Factor Updates Mid October.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=188](https://vote.onaave.com/proposal/?proposalId=188)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-polygon-v2-borrow-rate-adjustments/17252/13](https://governance.aave.com/t/arfc-polygon-v2-borrow-rate-adjustments/17252/13)

[https://governance.aave.com/t/arfc-avalanche-v2-reserve-factor-adjustment/17040/13](https://governance.aave.com/t/arfc-avalanche-v2-reserve-factor-adjustment/17040/13)

[https://governance.aave.com/t/arfc-ethereum-v2-reserve-factor-adjustment/16764/18](https://governance.aave.com/t/arfc-ethereum-v2-reserve-factor-adjustment/16764/18)

[https://governance.aave.com/t/arfc-increase-bridged-usdc-reserve-factor-across-all-deployments/17787/10](https://governance.aave.com/t/arfc-increase-bridged-usdc-reserve-factor-across-all-deployments/17787/10)
 
<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x8072ecc9C68915E949B6a899d6D46297C6C88838#code#F1#L1)

* Polygon V2 - [proposal payloads](https://polygonscan.com/address/0xC88C0309Bd7F22a716319246AAB7bB641C4CA03e#code#F1#L1)

* Polygon V3 - [proposal payloads](https://polygonscan.com/address/0xFdEE2D765aCc739fe1BC399316C4901c0E78aCf9#code#F1#L1)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xA7d6f775fD9E033b31A38e6ceD7E6Be8D02121A9/contract/43114/code)

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0x78dD3Bc46872E652f412271bDb682Aac2bEE30bE#code#F1#L1)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x8b9E6aAC8CFbD2a1B59a795eddc11bd3597eEcCA#code#F1#L1)

* Base - [proposal payloads](https://basescan.org/address/0x44F7f0C9C1e8B8430877C247Ab87B5fA7ae03752#code#F1#L1)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x941dFcB7698359da9b24DC54A14a730703F3fe8b#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal sets new reserves factor across Aave deployments and sets slope1 parameter on Polygon assets.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x30290721ed0473157448205357873f1062fdb083972a16b9a16875cd567e6463](https://etherscan.io/tx/0x30290721ed0473157448205357873f1062fdb083972a16b9a16875cd567e6463)

```
- proposalId: 188
- creator: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- accessLevel: 1
- ipfsHash: 0xb772c95bee85b137bb8b63e62f70427ff7f937514eda46aa757d4053e65ba5e9
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
      "payloadId": "195"
    },
    {
      "chain": "137",
      "accessLevel": "1",
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
      "payloadId": "87"
    },
    {
      "chain": "43114",
      "accessLevel": "1",
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
      "payloadId": "59"
    },
    {
      "chain": "10",
      "accessLevel": "1",
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
      "payloadId": "55"
    },
    {
      "chain": "42161",
      "accessLevel": "1",
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
      "payloadId": "57"
    },
    {
      "chain": "8453",
      "accessLevel": "1",
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
      "payloadId": "43"
    },
    {
      "chain": "100",
      "accessLevel": "1",
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
      "payloadId": "36"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0xb772c95bee85b137bb8b63e62f70427ff7f937514eda46aa757d4053e65ba5e9"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/188.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/188.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/195.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/195.md)

* Polygon - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/87.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/87.md)

* Avalanche - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/59.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/59.md)

* Optimism - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/55.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/55.md)

* Arbitrum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/57.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/57.md)

* Base - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/43.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/43.md)

* Gnosis - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/36.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/36.md)

<br>

### Technical analysis

We have confirmed that the payload successfully adjusts the slope1 for the specified assets on Polygon and have also verified that it updates the reserve factor across Aave deployments.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

