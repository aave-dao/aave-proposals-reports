# Proposal 82. Set Price Cap Adapters For Aave V2.

<br>

### Voting link

[https://vote.onaave.com/proposal/?proposalId=82](https://vote.onaave.com/proposal/?proposalId=82)

<br>

### Governance forum discussion

[https://governance.aave.com/t/bgd-technical-maintenance-proposals/15274/30](https://governance.aave.com/t/bgd-technical-maintenance-proposals/15274/30)

<br>

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x927402dF69eaDC67ab0Ce0D443dA87d04dcaD84A#code#F1#L1)

* Polygon - [proposal payloads](https://polygonscan.com/address/0xF70E9568Cc0E23154b1478356a1bCB75fD2d0D16#code#F1#L1)

* Avalanche - [proposal payloads](https://snowscan.xyz/address/0x3C27599160ed92bc62660c13E6F3F5930485F92B#code#F1#L1)

<br>

## Certora analysis

<br>

### Proposal types

:scroll::small_red_triangle: contract upgrade

<br>

### Context

This proposal activates the correlated-assets price oracle (CAPO) system for fiat-pegged stable coins and also updates price feeds on Aave-V2 in order to add an upper side protection.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x17913b20ab6fce7b9a0ff3c3b4095bc97515cd082e7e738c00abaa1ce4bc1e1c](https://etherscan.io/tx/0x17913b20ab6fce7b9a0ff3c3b4095bc97515cd082e7e738c00abaa1ce4bc1e1c)

```
- proposalId: 82
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- accessLevel: 1
- ipfsHash: 0x4886864ed1dc6cb220f17cd372697218cbb5c2ada41e63d6a1f7664168d59052
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
      "payloadId": "106" 
    }, 
    { 
      "chain": "137", 
      "accessLevel": "1", 
      "payloadsController": "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C", 
      "payloadId": "54" 
    }, 
    { 
      "chain": "43114", 
      "accessLevel": "1", 
      "payloadsController": "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80", 
      "payloadId": "25" 
    }, 
  ], 
  "votingPortal": "0x9b24C168d6A76b5459B1d47071a54962a4df36c3", 
  "ipfsHash": "0x4886864ed1dc6cb220f17cd372697218cbb5c2ada41e63d6a1f7664168d59052" 
}
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/82.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/82.md)

**Payload reports**

* Ethereum V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/106.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/106.md)

* Polygon V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/54.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/54.md)

* Avalanche V2 - [https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/25.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/25.md)

<br>

### Technical analysis

We have verified that the payload changes the Asset Source of the following tokens on the following chains:

- Ethereum:

    USDC: 0x9f2817536Cfd48BF59243d9D8802a5670F5Be05d

    USDT: 0xEfF57B0c8987eea8C491bdDD2F64c1c21297Cf74

    DAI: 0xd486FE27AAB0b3CAd1462D767292dd7a84F06E58

    USDP: 0x776292E6eb3eD2D28C0CFa77BaB9378A771424Be

    sUSD: 0x00753D870Ceda60b38A9efeb47a724160BD8A749

    FRAX: 0x1f7e2ccd6702a5c587160390A52111aF6020ac92

    LUSD: 0x3a1b874ec865c466046cf131516d26Cc228dF0b3

    BUSD: 0x378E959C0eCBbA793217913cE1D8745f6d6B7aC7 

    TUSD: 0x65f05c3bC078bf24EdeaCFD48D6312c103AC4a61

    UST: 0x51d08b4912d33d051b57d784c7CAfC0cD42c0f45

    DPI: 0x2fe9EcF3024B5A63f50Ec0eFC53b8fF2C09F2E93

- Polygon:

    USDC.e: 0xB611AA5E98112C7c3711Ca3a5187dC025B83C8e4

    DAI: 0x08EDd9E1DF3b0b8498864C60a2FD6cDb13148885

    USDT: 0xf840c80932908EF206056dF0882bC595e7150607

- Avalanche:

    USDC.e: 0xD8277249e871BE9A402fa286C2C5ec16046dC512

    DAI.e: 0xf82da795727633aFA9BB0f1B08A87c0F6A38723f

    USDT.e: 0x39185f2236A6022b682e8BB93C040d125DA093CF

<br>

The proposal is consistent with the description on the governance forum.

<br>

### Certora validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Certora reviewed the procedure followed to submit the proposal.
