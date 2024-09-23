# Proposal 170. Reserve Factor Updates Late September.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=170](https://vote.onaave.com/proposal/?proposalId=170)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-polygon-v2-borrow-rate-adjustments/17252/12](https://governance.aave.com/t/arfc-polygon-v2-borrow-rate-adjustments/17252/12)

[https://governance.aave.com/t/arfc-avalanche-v2-reserve-factor-adjustment/17040/12](https://governance.aave.com/t/arfc-avalanche-v2-reserve-factor-adjustment/17040/12)

[https://governance.aave.com/t/arfc-ethereum-v2-reserve-factor-adjustment/16764/17](https://governance.aave.com/t/arfc-ethereum-v2-reserve-factor-adjustment/16764/17)

[https://governance.aave.com/t/arfc-increase-bridged-usdc-reserve-factor-across-all-deployments/17787/9](https://governance.aave.com/t/arfc-increase-bridged-usdc-reserve-factor-across-all-deployments/17787/9)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xb62695372eAC5134a330AB0Aa6C22cdCB93Da051#code#F1#L1)

* Polygon - [proposal payloads](https://polygonscan.com/address/0xf7179bD6a888BfC14710241EFe706A576e3AFEe1#code#F1#L1)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xd5E1876D6bFe791f24Cf4302C21B76946Bcc1819/contract/43114/code)

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0x6F0aF154DCbFC8548261d658FD4FEDaBaA4388EA#code#F1#L1)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0xa6320cbae03018569fe0D3a0E620346862ddE470#code#F1#L1)

* Base - [proposal payloads](https://basescan.org/address/0x4cDbBb3883ac90E5c03e1a351aB561b678c00372#code#F1#L1)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0xBA944DbeD70E28B5dEB744F4Aa03bcd020d8e756#code#F1#L1)

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

Transaction: [https://etherscan.io/tx/0x9fd10d1268159b6e2443ae91cf04024ee0d2c44697fd989476b5c4e9eaec9e22](https://etherscan.io/tx/0x9fd10d1268159b6e2443ae91cf04024ee0d2c44697fd989476b5c4e9eaec9e22)

```
- proposalId: 170
- creator: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- accessLevel: 1
- ipfsHash: 0x9917a3e87db5eae531dfc2fa669caf3f75a5a22f450dd44e8fd7d445b66830a2
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
      "payloadId": "178"
    },
    {
      "chain": "137",
      "accessLevel": "1",
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
      "payloadId": "82"
    },
    {
      "chain": "43114",
      "accessLevel": "1",
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
      "payloadId": "53"
    },
    {
      "chain": "10",
      "accessLevel": "1",
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
      "payloadId": "49"
    },
    {
      "chain": "42161",
      "accessLevel": "1",
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
      "payloadId": "51"
    },
    {
      "chain": "8453",
      "accessLevel": "1",
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
      "payloadId": "37"
    },
    {
      "chain": "100",
      "accessLevel": "1",
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
      "payloadId": "31"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0x9917a3e87db5eae531dfc2fa669caf3f75a5a22f450dd44e8fd7d445b66830a2"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/170.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/170.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/178.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/178.md)

* Polygon - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/82.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/82.md)

* Avalanche - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/53.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/53.md)

* Optimism - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/49.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/49.md)

* Arbitrum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/51.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/51.md)

* Base - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/37.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/37.md)

* Gnosis - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/31.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/31.md)

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

