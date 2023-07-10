# Proposal 266. Aave v2 Ethereum - Reserve Factor updates

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=266](https://app.aave.com/governance/proposal/?proposalId=266)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-incremental-reserve-factor-updates-aave-v2-ethereum/13766](https://governance.aave.com/t/arfc-chaos-labs-incremental-reserve-factor-updates-aave-v2-ethereum/13766)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal increases the Reserve Factor parameter on multiple Aave v2 Ethereum assets, with the objective of incentivising migrations to Aave v3 Ethereum.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xd7b02f15f580414a8aa86be7c5321ce340a7bf1392bfe95d060a4c981cc57156](https://etherscan.io/tx/0xd7b02f15f580414a8aa86be7c5321ce340a7bf1392bfe95d060a4c981cc57156)

```
- id: 266
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xf64c196f2cd0d00d280140a138674efbace18572]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 17635960
- endBlock: 17655160
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xa8ff0f61c45be32c48b093f1277da0531a6c24ca3b32f4d05cc6a5d80655a2d0
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/266.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/266.md)


<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xf64c196f2cd0d00d280140a138674efbace18572#code#F1#L13) properly changes the following Reserve Factors on Aave v2 Ethereum:

TUSD: 5% -> **25%**

GUSD: 10% -> **15%**

1INCH: 20% -> **25%**

UNI: 20% -> **25%**

WBTC: 20% -> **25%**

LINK: 20% -> **25%**

sUSD: 20% -> **25%**

LUSD: 10% -> **15%**

DAI: 10% -> **15%**

FRAX: 20% -> **25%**

USDP: 10% -> **15%**

MKR: 20% -> **25%**

USDC: 10% -> **15%**

SNX: 35% -> **40%**

WETH: 15% -> **20%**

ENS: 20% -> **25%**

CRV: 20% -> **25%**

USDT: 10% -> **15%**



<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
