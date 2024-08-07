# Proposal 145. Reduce Reserve Factor on wstETH.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=145](https://vote.onaave.com/proposal/?proposalId=145)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-reduce-reserve-factor-on-wsteth/18044/1](https://governance.aave.com/t/arfc-reduce-reserve-factor-on-wsteth/18044/1)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x17A5eb41026DC9B410866228843dEF36aE147CE7#code#F1#L1)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x52157e47c323C3077Ede943B0B8ab43c52F24D6B#code#F1#L1)

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0x31587698b0bD75f2BcD9543b682E7e0C4B6F984d#code#F1#L1)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x2A99c608a90c9aE8EaD0c58AED36c0b42e8172ED#code#F1#L1)

* Base - [proposal payloads](https://basescan.org/address/0x81EEFff1AC6624707ac77C67d820849d3c4c0Ef9#code#F1#L1)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x5D62643c706a76Ecf0Ee474753Bf463a48F678b2#code#F1#L1)

* Scroll - [proposal payloads](https://scrollscan.com/address/0x2E2142dfa013578a3920b68c20d07F3d505A9E8c#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal reduces the reserve factor of wstETH across all V3-markets in order to further align with the upcoming Lido Alliance proposals.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xe7430927138f4cd1aacbb29779fefa01766b3ad4bf4a100203d34355bd051ac3](https://etherscan.io/tx/0xe7430927138f4cd1aacbb29779fefa01766b3ad4bf4a100203d34355bd051ac3)

```
- proposalId: 145
- creator: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- accessLevel: 1
- ipfsHash: 0x6985386cb307aa45146c8e2e1ab70a8807267646fb45791184af1a64dc15e8a8
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
      "payloadId": "157"
    },
    {
      "chain": "137",
      "accessLevel": "1",
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
      "payloadId": "75"
    },
    {
      "chain": "10",
      "accessLevel": "1",
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
      "payloadId": "42"
    },
    {
      "chain": "42161",
      "accessLevel": "1",
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
      "payloadId": "44"
    },
    {
      "chain": "8453",
      "accessLevel": "1",
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
      "payloadId": "28"
    },
    {
      "chain": "100",
      "accessLevel": "1",
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
      "payloadId": "27"
    },
    {
      "chain": "534352",
      "accessLevel": "1",
      "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE",
      "payloadId": "19"
    },
  ],
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
  "ipfsHash": "0x6985386cb307aa45146c8e2e1ab70a8807267646fb45791184af1a64dc15e8a8"
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/145.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/145.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/157.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/157.md)

* Polygon - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/75.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/75.md)

* Optimism - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/42.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/42.md)

* Arbitrum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/44.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/44.md)

* Base - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/28.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/28.md)

* Gnosis - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/27.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/27.md)

* Scroll - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/19_forge.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/19_forge.md)

<br>

### Technical analysis

We have verified that the payloads reduce the reserve factor of wstETH on all Aave-V3-Markets to 5%.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

