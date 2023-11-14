# Proposal 362. Aave v2 Ethereum - Risk parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=362](https://app.aave.com/governance/proposal/?proposalId=362)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-v2-ethereum-lt-reductions-10-27-2023/15249](https://governance.aave.com/t/arfc-v2-ethereum-lt-reductions-10-27-2023/15249)

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

Transaction: [https://etherscan.io/tx/0xd73831d9ef5b6770637b5e24fe87f195aadde9bb2218136cd9c66755ad1eaedb](https://etherscan.io/tx/0xd73831d9ef5b6770637b5e24fe87f195aadde9bb2218136cd9c66755ad1eaedb)

```
- id: 362
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9aee0b04504cef83a65ac3f0e838d0593bcb2bc7]
- values: [0]
- signatures: [forwardPayloadForExecution((uint256,uint8,address,uint40))]
- calldatas: [0x00000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000001000000000000000000000000dabad81af85554e9ae636395611c58f7ec1aaec50000000000000000000000000000000000000000000000000000000000000002]
- withDelegatecalls: [false]
- startBlock: 18529541
- endBlock: 18548741
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xb4f51e1760e48fe78974223d6e539f0eb40223b49ad48bbe2b8717fe553640d3
```

<br>

### Aave Seatbelt report

**Proposal report**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/362.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/362.md)

**Payloads report**

[https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/2.md](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/2.md)



<br>

### Technical analysis

We have verified the [proposal payload](https://etherscan.io/address/0xc62cAb55a4376F916D107D7e09356E9799c090fa#code#F1#L13) updates the following parameters on Aave v2 Ethereum, via its Pool Configurator contract:

YFI
- Liquidation Threshold: 45% -> **43%**

MANA
- Liquidation Threshold: 48% -> **37%**

1INCH
- Liquidation Threshold: 24% -> **1%**
- LTV: 30% -> **0%**

DPI:
- Liquidation threshold: 16% -> **14%**

UNI
- LTV: 70% -> **64%**

REN
- Liquidation Threshold: 27% -> **25%**

CVX
- Liquidation Threshold: 33% -> **30%**

LINK:
- Liquidation Threshold: 82% -> **81%**

XSUSHI
- Liquidation Threshold: 28% -> **1%**

MKR
- Liquidation Threshold: 35% -> **30%**

BAL
- Liquidation Threshold: 25% -> **21%**

SNX
- Liquidation Threshold: 43% -> **41%**

ENS
- Liquidation Threshold: 50% -> **47%**

CRV:
- Reserve Factor: 42% -> **38%**

ZRX
- Liquidation Threshold: 37% -> **34%**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
