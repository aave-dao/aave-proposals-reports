# Proposal 231. Aave v3 Polygon - WMATIC caps update

<br>


### Voting link

[https://app.aave.com/governance/proposal/?proposalId=231](https://app.aave.com/governance/proposal/?proposalId=231)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-wmatic-supply-borrow-cap-increase-polygon-v3-16-05-2023/13095](https://governance.aave.com/t/arfc-wmatic-supply-borrow-cap-increase-polygon-v3-16-05-2023/13095)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the supply and borrow caps of WMATIC on Aave v3 Polygon.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xa251b9b3bbe6cd0672770d2ea819b2d93a848778746a6cf0e5ab60ae2eb39b0a](https://etherscan.io/tx/0xa251b9b3bbe6cd0672770d2ea819b2d93a848778746a6cf0e5ab60ae2eb39b0a)

```
- id: 231
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x158a6bc04f0828318821bae797f50b0a1299d45b]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000eb06d30b4bb21ca98279b74fd2325b8f2759aa50]
- withDelegatecalls: [true]
- startBlock: 17302458
- endBlock: 17321658
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xbd4025b126376e7845780150adbe088f305d03bb15693e819a5819b03b3f3664
```

<br>

### Aave Seatbelt reports

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/231.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/231.md)

**Polygon**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/231_fx_41_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/231_fx_41_0.md)

<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Polygon.

From a technical perspective, we have verified the [proposal payload](https://polygonscan.com/address/0xeb06d30b4bb21ca98279b74fd2325b8f2759aa50#code#F23#L1) correctly uses the [BGD's Aave Config Engine of Aave v3 Polygon](https://polygonscan.com/address/0xe202f2fc4b6a37ba53cfd15be42a762a645fca07#code#F18#L1), in this case, to update both the supply and borrow caps of WMATIC  the following way:
- Supply cap: 66'000'000 WMATIC -> **90'000'000 WMATIC**
- Borrow cap: 39'950'000 WMATIC -> **50'000'000 WMATIC**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
