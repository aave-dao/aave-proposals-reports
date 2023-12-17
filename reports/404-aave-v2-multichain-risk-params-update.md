# Proposal 404. Aave v2 Ethereum, Polygon - Risk parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=404](https://app.aave.com/governance/proposal/?proposalId=404)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-v2-ethereum-and-polygon-lt-reductions-12-04-2023/15747](https://governance.aave.com/t/arfc-v2-ethereum-and-polygon-lt-reductions-12-04-2023/15747)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates multiple risk parameters on Aave v2 Ethereum and Polygon.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x10e407ef413ae3101adbf8fdc221c2e6bf74de2dc90f3416ddfad4c7c05eb0bc](https://etherscan.io/tx/0x10e407ef413ae3101adbf8fdc221c2e6bf74de2dc90f3416ddfad4c7c05eb0bc)

```
- id: 404
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7,0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0,0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40)),forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dabad81af85554e9ae636395611c58f7ec1aaec50000000000000000000000000000000000000000000000000000000000000024,0x00000000000000000000000000000000000000000000000000000000000000890000000000000000000000000000000000000000000000000000000000000001000000000000000000000000401b5d0294e23637c18fcc38b1bca814cda2637c0000000000000000000000000000000000000000000000000000000000000014]
- withDelegatecalls: [false,false]
- startBlock: 18789873
- endBlock: 18809073
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x3fbf5c863c25538b6cd4a917dd17c49221b7f2e7200f25400056de9c8fd08ddd
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/404.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/404.md)

**Payloads report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/36.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/36.md)

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/20.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/20.md)



<br>

### Technical analysis

The proposal contains 2 payloads, one for Ethereum and another for Polygon. Both change Liquidation Threshold and LTV parameters for different assets of each pool.

<br>

**[Ethereum payload](https://etherscan.io/address/0x41b08a9C1dddBfdBFBb46973A17f76FF06A7d3D6#code#F1#L13)**

YFI
- Liquidation Threshold: 32% -> **0.05%**

BAT
- Liquidation Threshold: 1% -> **0.05%**

MANA
- Liquidation Threshold: 29% -> **0.05%**

1INCH
- Liquidation Threshold: 1% -> **0.05%**

DPI:
- Liquidation threshold: 5% -> **0.05%**

UNI
- Liquidation Threshold: 55% -> **40%**

REN
- Liquidation Threshold: 18% -> **0.05%**

CVX
- Liquidation Threshold: 24% -> **0.05%**

LINK:
- Liquidation Threshold: 80% -> **75%**

xSUSHI
- Liquidation Threshold: 1% -> **0.05%**

FEI
- Liquidation Threshold: 1% -> **0.05%**

MKR
- Liquidation Threshold: 28% -> **26%**

BAL
- Liquidation Threshold: 1% -> **0.05%**

SNX
- Liquidation Threshold: 30% -> **0.05%**

ENS
- Liquidation Threshold: 38% -> **30%**

CRV:
- Liquidation Threshold: 30% -> **25%**

KNC
- Liquidation Threshold: 1% -> **0.05%**

ZRX
- Liquidation Threshold: 24% -> **18%**

ENJ
- Liquidation Threshold: 44% -> **0.05%**

<br>

**[Polygon payload](https://polygonscan.com/address/0xf64C196f2Cd0D00D280140a138674EFbacE18572#code#F1#L13)**

SUSHI
- LTV: 20% -> **0%**
- Liquidation Threshold: 45% -> **0.05%**

CRV
- LTV: 20% -> **0%**
- Liquidation Threshold: 45% -> **0.05%**

GHST
- LTV: 25% -> **0%**
- Liquidation Threshold: 40% -> **0.05%**

LINK
- LTV: 50% -> **0%**
- Liquidation Threshold: 65% -> **0.05%**

DPI
- LTV: 20% -> **0%**
- Liquidation Threshold: 45% -> **0.05%**

BAL
- LTV: 20% -> **0%**
- Liquidation Threshold: 45% -> **0.05%**

<br>

The proposal payloads are consistent with the description on the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
