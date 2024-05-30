# Proposal 111. Ethereum + Avalanche v2 Reserve Factor Updates.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=111](https://vote.onaave.com/proposal/?proposalId=111)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-ethereum-v2-reserve-factor-adjustment/16764/10](https://governance.aave.com/t/arfc-ethereum-v2-reserve-factor-adjustment/16764/10)

[https://governance.aave.com/t/arfc-avalanche-v2-reserve-factor-adjustment/17040/5](https://governance.aave.com/t/arfc-avalanche-v2-reserve-factor-adjustment/17040/5)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xd15A85FD4AdBE6D5256279534f2Ca46Ca5159e00#code#F1#L1)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0xa96dB8D886ACa0Fa3D76e6187B300a7924C6977E/contract/43114/code)

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

Transaction: [https://etherscan.io/tx/0xb8a6492ed5d78f3a22e935ede94e4a66768981202759db96632f6abb3414b0cd](https://etherscan.io/tx/0xb8a6492ed5d78f3a22e935ede94e4a66768981202759db96632f6abb3414b0cd)

```
- proposalId: 111
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0x6020305b890026e953ce2ba1087cc9dabad7fbafc9ce23234904615e5696ea1e
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
      "payloadId": "131" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "37" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x6020305b890026e953ce2ba1087cc9dabad7fbafc9ce23234904615e5696ea1e" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/111.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/111.md)

**Payload reports**

* Ethereum V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/131.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/131.md)

* Avalanche V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/37.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/37.md)

<br>

### Technical analysis

We have verified that the payload modifies the reserve factor of the following tokens to the following values:

- Ethereum V2:

    DAI: 55.00%

    FRAX: 99.99%

    GUSD: 99.99%

    LINK: 60.00%

    LUSD: 99.99%

    sUSD: 99.99%

    USDC: 55.00%

    USDP: 99.99%

    USDT: 55.00%

    WBTC: 60.00%

    WETH: 55.00%

- Avalanche V2:

    DAIe: 50.00%

    USDCe: 50.00%

    USDTe: 50.00%

    WAVAX: 50.00%

    WBTCe: 55.00%

    WETHe: 50.00%

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
