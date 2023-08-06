# Proposal 286. Aave v2 Ethereum - CRV risk parameters update

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=286](https://app.aave.com/governance/proposal/?proposalId=286)

<br>

### Governance forum discussion

[https://governance.aave.com/t/post-vyper-exploit-crv-market-update-and-recommendations/14214/4](https://governance.aave.com/t/post-vyper-exploit-crv-market-update-and-recommendations/14214/4)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal sets the LTV of CRV to 0%, not allowing to increase borrowings against CRV via borrow().

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x9485d5a2c2e066112d8521473da2db1f21952c2a775d59fc6b9054bbd61f3ce2](https://etherscan.io/tx/0x9485d5a2c2e066112d8521473da2db1f21952c2a775d59fc6b9054bbd61f3ce2)

```
- id: 286
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x311bb771e4f8952e6da169b425e7e92d6ac45756]
- values: [0]
- signatures: [configureReserveAsCollateral(address,uint256,uint256,uint256)]
- calldatas: [0x000000000000000000000000d533a949740bb3306d119cc777fa900ba034cd520000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000157c0000000000000000000000000000000000000000000000000000000000002a30]
- withDelegatecalls: [false]
- startBlock: 17829625
- endBlock: 17848825
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x17a1ed9e14b4fa2dfcddd11503fd86d080b33d266061fe7953b2db0ed3cac920
```

<br>

### Aave Seatbelt report

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/286.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/286.md)


<br>

### Technical analysis

We have verified the proposal payload (submitted via calldata, not delegatecall) properly sets the LTV of CRV to 0% (from 49%), by calling `configureReserveAsCollateral()` on the PoolConfigurator of Aave v2 Ethereum.

The proposal is consistent with the discussions on the Aave governance forum.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the payload before the proposal was submitted.

:x: Only one payload used via delegatecall

:x: BGD reviewed the procedure followed to submit the proposal.
