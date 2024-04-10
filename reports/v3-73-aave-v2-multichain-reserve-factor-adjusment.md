# Proposal 73. Ethereum + Avalanche v2 Reserve Factor Adjustment.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=73](https://vote.onaave.com/proposal/?proposalId=73)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-ethereum-v2-reserve-factor-adjustment/16764/6](https://governance.aave.com/t/arfc-ethereum-v2-reserve-factor-adjustment/16764/6)

[https://governance.aave.com/t/arfc-avalanche-v2-reserve-factor-adjustment/17040](https://governance.aave.com/t/arfc-avalanche-v2-reserve-factor-adjustment/17040)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xce671a877660A96508ACC5566c829568Fd7e1114#code#F1#L1)

* Avalanche - [proposal payloads](https://snowscan.xyz/address/0x7Cc9EF92D76CbDdFfEBD53C75084D8FA29f695Ec#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal increases the reserve factors of multiple assets on Aave-V2-Ethereum and Aave-V2-Avalanche by 5% up to 99.99% in order to encouraging users to migrate from Ethereum v2 to v3. 

For Avalanche the reserve factors values will be aligned with the Ethereum v2 deployment.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x21ee08bbdb417280920defe72e5107a8753b014b47a0aa8f903e31d260a7f71b](https://etherscan.io/tx/0x21ee08bbdb417280920defe72e5107a8753b014b47a0aa8f903e31d260a7f71b)

```
- proposalId: 73
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xf8fc52827b51bfa6db62842715fc2972fb32384c87d3e072a710ea02abe83962
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
      "payloadId": "100" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "23" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xf8fc52827b51bfa6db62842715fc2972fb32384c87d3e072a710ea02abe83962" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/73.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/73.md)

**Payload reports**

* Ethereum V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/100.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/100.md)

* Avalanche V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/23.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/23.md)

<br>

### Technical analysis

We have verified that the payload modifies the reserve factor of the following tokens to the following values:

- Ethereum V2:

    DAI: 40.00%

    FRAX: 45.00%

    GUSD: 35.00%

    LINK: 45.00%

    LUSD: 40.00%

    sUSD: 45.00%

    USDC: 40.00%

    USDP: 35.00%

    USDT: 40.00%

    WBTC: 45.00%

    WETH: 40.00%

- Avalanche V2:

    DAIe: 35.00%

    USDCe: 35.00%

    USDTe: 35.00%

    WAVAX: 35.00%

    WBTCe: 40.00%

    WETHe: 35.00%

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
