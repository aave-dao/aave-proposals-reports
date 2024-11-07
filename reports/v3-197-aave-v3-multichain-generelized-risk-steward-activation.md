# Proposal 197. Aave Generalized Risk Stewards (AGRS) activation


<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=197](https://vote.onaave.com/proposal/?proposalId=197)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-aave-generalized-risk-stewards-agrs-activation/19178](https://governance.aave.com/t/arfc-aave-generalized-risk-stewards-agrs-activation/19178)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xD38E07fc60889Fa7EfbD02F259d7D39805dDFbef#code#F1#L1)

* EthereumLido - [proposal payloads](https://etherscan.io/address/0x0E1736f9594217bB42a56828586d5A26e9480f0D#code#F1#L1)

* Ethereum EtherFi - [proposal payloads](https://etherscan.io/address/0xDD47D2b4FBB81FC8f631AbF044c4ba6C34CC2606#code#F1#L1)

* Polygon - [proposal payloads](https://polygonscan.com/address/0x5B615173Dc67084172970d3FbaB27D80c7970212#code#F1#L1)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xBaFCB2429Fed19D20f2b45238190c83a4fe7dC2B/contract/43114/code)

* Optimism - [proposal payloads](https://optimistic.etherscan.io/address/0xb6360a6f29EDB873814a75FC5F2BC43675c207b2#code#F1#L1)

* Arbitrum - [proposal payloads](https://arbiscan.io/address/0x8243561fd89b3c2C794AbB68951e1ab8C7d33281#code#F1#L1)

* Metis - [proposal payloads](https://explorer.metis.io/address/0x00485caDaab82B196Ad4aBCFa632Fe070Aa8Ea65/contract/1088/code)

* Base - [proposal payloads](https://basescan.org/address/0x0783E360Ad12784037eA1c48c8Aa6F8E3C11740A#code#F1#L1)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x406787aA83503C8e2414692d00Caa1AAbcdFAE64#code#F1#L1)

* Scroll - [proposal payloads](https://scrollscan.com/address/0x97581dEC936B77f53815197B7a23121657dbEfc7#code#F1#L1)

* BNB - [proposal payloads](https://bscscan.com/address/0x5CB878e88505486872A90d7a77b63a1aE68174BE#code#F1#L1)

* zkSync - [proposal payloads](https://era.zksync.network//address/0x784588812a920C75afAaC00CBaFCCc8fE0d760D8#code#F1#L1)


<br>

## Certora analysis

<br>

### Proposal types

:handshake: permission granting or revoking

<br>

### Context

This AIP activates the Manual AGRS and the Automated AGRS will be activated at a later stage. Expanding from the scope of CapsPlusRiskSteward, we now introduce the new Aave Generalized Risk Stewards (AGRS), allowing hardly constrained risk parameter updates by risk service providers and reducing governance overhead.



<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x112e064e54faee86b04eb0875b190cedaa3e66e7b5b6d2b76a1207bddc7ed76e](https://etherscan.io/tx/0x112e064e54faee86b04eb0875b190cedaa3e66e7b5b6d2b76a1207bddc7ed76e)

```
- proposalId: 197
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0x2f41406557b0fc69c256916c066a77c57434fa77ccab3cfe56c8db6a4f306c01
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
      "payloadId": "203" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "88" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "60" 
    }, 
    { 
      "chain": "10", 
      "accessLevel": "1", 
      "payloadsController": "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4", 
      "payloadId": "56" 
    }, 
    { 
      "chain": "42161", 
      "accessLevel": "1", 
      "payloadsController": "0x89644CA1bB8064760312AE4F03ea41b05dA3637C", 
      "payloadId": "59" 
    }, 
    { 
      "chain": "1088", 
      "accessLevel": "1", 
      "payloadsController": "0x2233F8A66A728FBa6E1dC95570B25360D07D5524", 
      "payloadId": "29" 
    }, 
    { 
      "chain": "8453", 
      "accessLevel": "1", 
      "payloadsController": "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01", 
      "payloadId": "44" 
    }, 
    { 
      "chain": "100", 
      "accessLevel": "1", 
      "payloadsController": "0x9A1F491B86D09fC1484b5fab10041B189B60756b", 
      "payloadId": "37" 
    }, 
    { 
      "chain": "534352", 
      "accessLevel": "1", 
      "payloadsController": "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE", 
      "payloadId": "27" 
    }, 
    { 
      "chain": "56", 
      "accessLevel": "1", 
      "payloadsController": "0xE5EF2Dd06755A97e975f7E282f828224F2C3e627", 
      "payloadId": "27" 
    }, 
    { 
      "chain": "324", 
      "accessLevel": "1", 
      "payloadsController": "0x2E79349c3F5e4751E87b966812C9E65E805996F1", 
      "payloadId": "8" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x2f41406557b0fc69c256916c066a77c57434fa77ccab3cfe56c8db6a4f306c01" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/197.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/197.md)

**Payload reports**

* Ethereum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/203.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/203.md)

* Polygon - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/88.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/88.md)

* Avalanche - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/60.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/57.md)

* Optimism - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/56.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/53.md)

* Arbitrum - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/59.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/55.md)

* Base - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/44.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/44.md)

* Gnosis - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/37.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/37.md)

* BNB - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/27.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/56/0xE5EF2Dd06755A97e975f7E282f828224F2C3e627/27.md)

<br>

### Technical analysis

We have verified that the proposal successfully activates the new Risk Steward contract. We compared the addresses specified on IPFS with the payload details, ensuring consistency. Additionally, we confirmed that the multisig ownership includes only Chaos Labs at the address 0x5d49dBcdd300aECc2C311cFB56593E71c445d60d.

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.

