# Proposal 314. Aave v3 Polygon - Caps update

<br>


### Voting link

[https://app.aave.com/governance/proposal/?proposalId=314](https://app.aave.com/governance/proposal/?proposalId=314)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-supply-cap-increase-lsts-on-polygon-v3/14696](https://governance.aave.com/t/arfc-supply-cap-increase-lsts-on-polygon-v3/14696)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the supply caps stMATIC and wstETH on Aave v3 Polygon.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x4599a6c7fc4feaaa8fcf5ddf7be939f05a550b44c7a7e3adf4c023e7455e26d5](https://etherscan.io/tx/0x4599a6c7fc4feaaa8fcf5ddf7be939f05a550b44c7a7e3adf4c023e7455e26d5)

```
- id: 314
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x0000000000000000000000009951f4eec081ce1ba383261b1acb2711b5e7631b]
- withDelegatecalls: [true]
- startBlock: 18077197
- endBlock: 18096397
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x7d9b85ffd89c168d825f747eed98b46f40717d1e3dec8f1ee13edb5661799430
```

<br>

### Aave Seatbelt reports

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/314.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/314.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/314_Polygon_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/314_Polygon_pending_0.md)

<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Polygon.

From a technical perspective, we have verified the [proposal payload](https://polygonscan.com/address/0x9951f4eec081ce1ba383261b1acb2711b5e7631b#code#F1#L13) correctly uses the BGD's Aave Config Engine of Aave v3 Polygon, in this case, to update the following caps:

stMATIC
- Supply cap: 57'000'000 stMATIC -> **66'000'000 stMATIC**

wstETH
- Supply cap: 3'450 wstETH -> **4'125 wstETH**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
