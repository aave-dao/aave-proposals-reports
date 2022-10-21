# Proposal 110. FEI Reserve Factor update (Aave v2 Ethereum)

<br>

### Voting link
[https://app.aave.com/governance/proposal/?proposalId=110](https://app.aave.com/governance/proposal/?proposalId=110)

<br>

### Governance forum discussion
[https://governance.aave.com/t/bgd-aave-v2-ethereum-fei-security-report/10251](https://governance.aave.com/t/bgd-aave-v2-ethereum-fei-security-report/10251)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

:ice_cube: freeze-asset

<br>

### Context
This proposal fixes a problem detected on proposal 96 when setting the Reserve Factor of FEI to 100%, by reducing it to 99%.

<br>

### Proposal creation
Transaction: [https://etherscan.io/tx/0x0a6d0712727fb053547bf6c1849cee055f7a7113cd87b97908fbef547cf870eb](https://etherscan.io/tx/0x0a6d0712727fb053547bf6c1849cee055f7a7113cd87b97908fbef547cf870eb)

```
- id: 110
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x993ee4acc9f736fd3e47846d18b397d06b899112]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 15783853
- endBlock: 15803053
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xdb0ac263eceb481e437f455dd309d42d1313489ce25c27e39cfae9a5b513672c
```

<br>

### Technical analysis
We have verifier the proposal payload does the following:

1. Sets the Reserve Factor for FEI to 99%, via the [PoolConfigurator](https://etherscan.io/address/0x311Bb771e4F8952E6Da169b425E7e92d6Ac45756).
2. In addition, if there is available liquidity on FEI, the payload will communicate with the Swapper smart contract deployed on proposal 96, in order to exchange FEI to aDAI. This action will also update the indexes of FEI (liquidity/borrow variable), that don't get updated automatically when doing a `setReserveFactor()`.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

:white_check_mark: Only one payload used via delegatecall
