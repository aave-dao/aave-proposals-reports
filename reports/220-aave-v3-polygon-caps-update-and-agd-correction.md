# Proposal 220. Aave v3 Polygon - Caps update


<br>


### Voting link

[https://app.aave.com/governance/proposal/?proposalId=220](https://app.aave.com/governance/proposal/?proposalId=220)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-maticx-supply-cap-increase-polygon-v3/12657](https://governance.aave.com/t/arfc-maticx-supply-cap-increase-polygon-v3/12657)

[https://governance.aave.com/t/updated-proposal-aave-grants-dao-renewal/11289/9](https://governance.aave.com/t/updated-proposal-aave-grants-dao-renewal/11289/9)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the supply cap of MATICX on Aave v3 Polygon.

Additionally, it gives allowance of aUSDT Aave v2 to Aave Grants DAO, replacing the wrong allowance of aUSDT Aave v1.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x5b98c853524ecb168bb2151ff8859aff7313785773ea1709e14741a652c1e2b8](https://etherscan.io/tx/0x5b98c853524ecb168bb2151ff8859aff7313785773ea1709e14741a652c1e2b8)

```
- id: 220
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x7be4fa90565d6fd6f7091d0af9e5a7f9cd7918a6,0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0,0]
- signatures: [execute(),execute(address)]
- calldatas: [0x,0x00000000000000000000000022c669eedf6e58de81777692b070cdb7432a4f84]
- withDelegatecalls: [true,true]
- startBlock: 17224367
- endBlock: 17243567
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xa3267468b4d12df2ded6b48eea658134acfb9e512b2b34ca9299fde49062531f
```

<br>

### Aave Seatbelt reports

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/220.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/220.md)


**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/220_fx_35_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/220_fx_35_0.md)


<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system for the payload interacting with Polygon.

Regarding the changes, we verified they are the following:

**[Ethereum](https://etherscan.io/address/0x7be4fa90565d6fd6f7091d0af9e5a7f9cd7918a6#code#F6#L1)**

The payload correctly reduces the allowance of aUSDT Aave v1 to 0, and replaces it with allowance of 812'944.90 aUSDT Aave v2.

**[Polygon](https://polygonscan.com/address/0x22c669eedf6e58de81777692b070cdb7432a4f84#code#F23#L1)**

The payload correctly updates the supply cap of MATICX from 17'200'000 MATIC to **29'300'000 MATICX**.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
