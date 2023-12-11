# Proposal 397. Aave v2 Ethereum - Rate strategies and Reserve Factor update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=397](https://app.aave.com/governance/proposal/?proposalId=397)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-rf-and-ir-updates-aave-v2-ethereum-2023-11-24/15661](https://governance.aave.com/t/arfc-chaos-labs-rf-and-ir-updates-aave-v2-ethereum-2023-11-24/15661)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates multiple interest rate strategies and reserve factors of frozen assets in Aave v2 Ethereum, to progress in the pool deprectation.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xea8fb4401dd9daa42860531e814ecfd96e324441cfd53407044bd29203326a43](https://etherscan.io/tx/0xea8fb4401dd9daa42860531e814ecfd96e324441cfd53407044bd29203326a43)

```
- id: 397
- creator: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dabad81af85554e9ae636395611c58f7ec1aaec5000000000000000000000000000000000000000000000000000000000000001e]
- withDelegatecalls: [false]
- startBlock: 18743669
- endBlock: 18762869
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x6a652079bf1999538d34c8d0692dff156d8905258df798d9fb1a24c68fd15e1f
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/397.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/397.md)

**Payloads report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/30.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/30.md)



<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xBE90E16CA2f6d2e0b828164Ef644f189d24D91bA#code#F1#L16) updates the following parameters on Aave v2 Ethereum, via its Pool Configurator contract and the BGD config engine:

RAI
- Reserve factor: 20% -> **99%**
- Base variable borrow rate: 0% -> **20%**
- Slope 1: 7% -> **0%**
- Slope 2: 75% -> **300%**

YFI
- Reserve factor: 35% -> **99%**
- Base variable borrow rate: 0% -> **20%**
- Slope 1: 7% -> **0%**

BAT
- Reserve factor: 35% -> **99%**
- Base variable borrow rate: 0% -> **20%**
- Slope 1: 7% -> **0%**

MANA
- Reserve factor: 50% -> **99%**
- Base variable borrow rate: 0% -> **20%**
- Slope 1: 7% -> **0%**

1INCH
- Reserve factor: 30% -> **99%**
- Base variable borrow rate: 0% -> **20%**
- Slope 1: 7% -> **0%**

DPI
- Reserve factor: 35% -> **99%**
- Base variable borrow rate: 0% -> **20%**
- Slope 1: 7% -> **0%**

UNI
- Reserve factor: 30% -> **99%**
- Base variable borrow rate: 0% -> **20%**
- Slope 1: 7% -> **0%**

REN
- Reserve factor: 35% -> **99%**
- Base variable borrow rate: 0% -> **20%**
- Slope 1: 7% -> **0%**

CVX
- Reserve factor: 35% -> **99%**
- Base variable borrow rate: 0% -> **20%**
- Slope 1: 7% -> **0%**

xSUSHI
- Reserve factor: 50% -> **99%**
- Base variable borrow rate: 0% -> **20%**
- Slope 1: 7% -> **0%**

MKR
- Reserve factor: 30% -> **99%**
- Base variable borrow rate: 0% -> **20%**
- Slope 1: 7% -> **0%**

UST
- Reserve factor: 20% -> **99%**
- Base variable borrow rate: 0% -> **20%**
- Slope 1: 4% -> **0%**
- Slope 2: 75% -> **300%**

BAL
- Reserve factor: 35% -> **99%**
- Base variable borrow rate: 5% -> **20%**
- Slope 1: 22% -> **0%**
- Slope 2: 150% -> **300%**

SNX
- Reserve factor: 45% -> **99%**
- Base variable borrow rate: 3% -> **20%**
- Slope 1: 12% -> **0%**
- Slope 2: 100% -> **300%**

ENS
- Reserve factor: 30% -> **99%**
- Base variable borrow rate: 0% -> **20%**
- Slope 1: 7% -> **0%**

AMPL
- Reserve factor: 10% -> **99%**
- Base variable borrow rate: 1% -> **20%**
- Slope 1: 2% -> **0%**
- Slope 2: 750% -> **300%**

CRV
- Reserve factor: 30% -> **99%**
- Base variable borrow rate: 3% -> **20%**
- Slope 1: 14% -> **0%**

KNC
- Reserve factor: 30% -> **99%**
- Base variable borrow rate: 0% -> **20%**
- Slope 1: 8% -> **0%**

ZRX
- Reserve factor: 35% -> **99%**
- Base variable borrow rate: 0% -> **20%**
- Slope 1: 7% -> **0%**

ENJ
- Reserve factor: 35% -> **99%**
- Base variable borrow rate: 0% -> **20%**
- Slope 1: 7% -> **0%**

<br>

The proposal slightly deviates from the description by setting RF lower (99%) than as it is described (99.9%). This doesn't create any problem for Aave, but we have communicated about this to the proposal creator.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
