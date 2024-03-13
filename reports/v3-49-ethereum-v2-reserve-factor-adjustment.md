# Proposal 49. Ethereum v2 Reserve Factor Adjustment.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=49](https://vote.onaave.com/proposal/?proposalId=49)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-ethereum-v2-reserve-factor-adjustment/16764](https://governance.aave.com/t/arfc-ethereum-v2-reserve-factor-adjustment/16764)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xc7c080511aDCE1e4728ab4e28A31D97243d1C581#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:wrench: :bar_chart: configuration update

<br>

### Context

This proposal increases the reserve factors of multiple assets on Aave-V2-Ethereum by 5% up to 99.99% in order to encouraging users to migrate from Ethereum v2 to v3.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xaedd234a46920bf0a4d97dcca9d41ce2b3eda12262b04b337404c66f89129840](https://etherscan.io/tx/0xaedd234a46920bf0a4d97dcca9d41ce2b3eda12262b04b337404c66f89129840)

```
- proposalId: 49
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- accessLevel: 1
- ipfsHash: 0xd0254523d65549ea7d020d91df2b7905a27da988ecc8263f2cf2709c2e369cc7
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
      "payloadId": "79" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0xd0254523d65549ea7d020d91df2b7905a27da988ecc8263f2cf2709c2e369cc7" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/49.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/49.md)

**Payload reports**

* Ethereum V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/79.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/79.md)

<br>

### Technical analysis

We have verified that the payload modifies the reserve factor of the following tokens to the following values:

TUSD: 99.99%

RAI: 99.99%

YFI: 99.99%

BAT: 99.99%

MANA: 99.99%

1INCH: 99.99%

DPI: 99.99%

UNI: 99.99%

REN: 99.99%

CVX: 99.99%

BUSD: 99.99%

xSUSHI: 99.99%

FEI: 99.99%

MKR: 99.99%

UST: 99.99%

BAL: 99.99%

SNX: 99.99%

ENS: 99.99%

AMPL: 99.99%

CRV: 99.99%

KNC: 99.99%

ZRX: 99.99%

ENJ: 99.99%

USDT: 30%

WETH: 30%

USDC: 30%

USDP: 25%

LUSD: 30%

DAI: 30%

FRAX: 35%

LINK: 35%

sUSD: 35%

WBTC: 35%

GUSD: 25%

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions. 

:white_check_mark: BGD reviewed the payload before the proposal was submitted. 

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
