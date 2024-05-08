# Proposal 102. Ethereum + Avalanche v2 Reserve Factor Updates.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=102](https://vote.onaave.com/proposal/?proposalId=102)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-ethereum-v2-reserve-factor-adjustment/16764/8](https://governance.aave.com/t/arfc-ethereum-v2-reserve-factor-adjustment/16764/8)

[https://governance.aave.com/t/arfc-avalanche-v2-reserve-factor-adjustment/17040/4](https://governance.aave.com/t/arfc-avalanche-v2-reserve-factor-adjustment/17040/4)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xDCfe7e4ED303ae88F312C248B83141DCd1A4a78a#code#F1#L1)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x0659a5d694FfE306B8e1d3F4CC887c67bdD9C753/contract/43114/code)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal increases the reserve factors of multiple assets on Aave-V2-Ethereum and Aave-V2-Avalanche by 5% up to 99.99% in order to encouraging users to migrate from v2 to v3. 

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x414e22fb5194a9155055c1b0750e7ffec3a9d2b247e94a9650f5361ef0e289db](https://etherscan.io/tx/0x414e22fb5194a9155055c1b0750e7ffec3a9d2b247e94a9650f5361ef0e289db)

```
- proposalId: 102
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x719cee2cd740d25f0ef3237ab7394bd92bc4e85b8c371fcf9006dd4b0a323d9a
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
      "payloadId": "124" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "33" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x719cee2cd740d25f0ef3237ab7394bd92bc4e85b8c371fcf9006dd4b0a323d9a" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/102.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/102.md)

**Payload reports**

* Ethereum V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/124.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/124.md)

* Avalanche V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/33.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/33.md)

<br>

### Technical analysis

We have verified that the payload modifies the reserve factor of the following tokens to the following values:

- Ethereum V2:

    DAI: 50.00%

    FRAX: 55.00%

    GUSD: 45.00%

    LINK: 55.00%

    LUSD: 50.00%

    sUSD: 55.00%

    USDC: 50.00%

    USDP: 45.00%

    USDT: 50.00%

    WBTC: 55.00%

    WETH: 50.00%

- Avalanche V2:

    DAIe: 45.00%

    USDCe: 45.00%

    USDTe: 45.00%

    WAVAX: 45.00%

    WBTCe: 50.00%

    WETHe: 45.00%

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
