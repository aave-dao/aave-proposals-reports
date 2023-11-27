# Proposal 383. Aave v2 Ethereum - Risk parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=383](https://app.aave.com/governance/proposal/?proposalId=383)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-v2-ethereum-deprecation-11-20-2023/15628](https://governance.aave.com/t/arfc-v2-ethereum-deprecation-11-20-2023/15628)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates multiple risk parameters on Aave v2 Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x1ece8f4458fdb641217c971c4237cafb5dd541d84efbf3539120b98418716ff4](https://etherscan.io/tx/0x1ece8f4458fdb641217c971c4237cafb5dd541d84efbf3539120b98418716ff4)

```
- id: 383
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dabad81af85554e9ae636395611c58f7ec1aaec50000000000000000000000000000000000000000000000000000000000000017]
- withDelegatecalls: [false]
- startBlock: 18637784
- endBlock: 18656984
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x4a54b101821f12b78ac4215ac84658d9ef6278a814267264728f2c57e998f83f
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/383.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/383.md)

**Payloads report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/23.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/23.md)



<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0x47a200a4805297c396aE73FFD52044D1Edb261bA#code#F1#L13) updates the following parameters on Aave v2 Ethereum, via its Pool Configurator contract:

YFI
- Liquidation Threshold: 43% -> **32%**

MANA
- Liquidation Threshold: 37% -> **29%**

DPI:
- Liquidation threshold: 14% -> **5%**

UNI
- Liquidation Threshold: 64% -> **55%**

REN
- Liquidation Threshold: 25% -> **18%**

CVX
- Liquidation Threshold: 30% -> **24%**

LINK:
- Liquidation Threshold: 81% -> **80%**

MKR
- Liquidation Threshold: 30% -> **28%**

SNX
- Liquidation Threshold: 41% -> **30%**

ENS
- Liquidation Threshold: 47% -> **38%**

CRV:
- Liquidation Threshold: 38% -> **30%**

ZRX
- Liquidation Threshold: 34% -> **24%**

ENJ
- Liquidation Threshold: 50% -> **44%**

BAL
- Liquidation Threshold: 21% -> **1%**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
