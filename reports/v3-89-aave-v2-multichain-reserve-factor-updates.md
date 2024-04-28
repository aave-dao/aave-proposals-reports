# Proposal 89. Ethereum + Avalanche v2 Reserve Factor Updates.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=89](https://vote.onaave.com/proposal/?proposalId=89)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-ethereum-v2-reserve-factor-adjustment/16764/7](https://governance.aave.com/t/arfc-ethereum-v2-reserve-factor-adjustment/16764/7)

[https://governance.aave.com/t/arfc-avalanche-v2-reserve-factor-adjustment/17040/3](https://governance.aave.com/t/arfc-avalanche-v2-reserve-factor-adjustment/17040/3)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x7506B338D79D40C69e7D228EFb348a79e09c4c73#code#F1#L1)

* Avalanche - [proposal payloads](https://snowscan.xyz/address/0xf67d117eaf79Df3BC7689A0b455734Ce4d34C282#code#F1#L1)

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

Transaction: [https://etherscan.io/tx/0x7c7f349dc6f76b0f0c8f6139282ae72dd169f9d535d31430f24f32b22c23e1a1](https://etherscan.io/tx/0x7c7f349dc6f76b0f0c8f6139282ae72dd169f9d535d31430f24f32b22c23e1a1)

```
- proposalId: 89
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xdafd69363854d3410239f3b9e3fa36a0e977a413e55dcf4e4d21c615173a2890
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
      "payloadId": "113" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "30" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xdafd69363854d3410239f3b9e3fa36a0e977a413e55dcf4e4d21c615173a2890" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/89.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/89.md)

**Payload reports**

* Ethereum V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/113.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/113.md)

* Avalanche V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/30.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/30.md)

<br>

### Technical analysis

We have verified that the payload modifies the reserve factor of the following tokens to the following values:

- Ethereum V2:

    DAI: 45.00%

    FRAX: 50.00%

    GUSD: 40.00%

    LINK: 50.00%

    LUSD: 45.00%

    sUSD: 50.00%

    USDC: 45.00%

    USDP: 40.00%

    USDT: 45.00%

    WBTC: 50.00%

    WETH: 45.00%

- Avalanche V2:

    DAIe: 40.00%

    USDCe: 40.00%

    USDTe: 40.00%

    WAVAX: 40.00%

    WBTCe: 45.00%

    WETHe: 40.00%

<br>

The proposal is consistent with the description on both Snapshot and the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
