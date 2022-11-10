# Proposal 115. Acquisition of 100'000 BAL by the Aave DAO

<br>

### Voting link
[https://app.aave.com/governance/proposal/?proposalId=115](https://app.aave.com/governance/proposal/?proposalId=115)

<br>

### Governance forum discussion
[https://governance.aave.com/t/arc-strategic-partnership-with-balancer-part-2/7813](https://governance.aave.com/t/arc-strategic-partnership-with-balancer-part-2/7813)

<br>

## BGD analysis

<br>

### Proposal types

:credit_card: funds-allowance

<br>

### Context
This proposal approves 800'000 aUSDC to be transferred from the Aave v2 Ethereum Collector to an smart contract that will manage partially spending them to acquire a maximum of 100'000 BAL.

<br>

### Proposal creation
Transaction: [https://etherscan.io/tx/0xe673b1b358c7e38cd9c13f8764b58e1c3c6b86e2f24f11c50cfbd8eee94eab40](https://etherscan.io/tx/0xe673b1b358c7e38cd9c13f8764b58e1c3c6b86e2f24f11c50cfbd8eee94eab40)

```
- id: 115
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x5e945515a8e1008dac95404aec9e12a9e65948f1]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 15935538
- endBlock: 15954738
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xdfd182646617ebe3360a602fe20c2688f04e2b848d8fb14adc1cebc53fc3d439
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/115.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/115.md)


<br>

### Technical analysis

The proposal payload in this case is really simple, only interacting with the [AaveEcosystemReserveController](https://etherscan.io/address/0x3d569673dAa0575c936c7c67c4E6AedA69CC630C#code) to give allowance of 800'000 aUSDC to an [OneWayBondingCurve smart contract](https://etherscan.io/address/0x04f90d449D4f8316eDd6Ef4F963b657f8444a4cA#code)


In addition to reviewing the payload, we have also checked the aforementioned OneWayBondingCurve. The exchange mechanism to acquired BAL from aUSDC to the Aave collector works as follows:
- The contract assumes having allowance of aUSDC. The 800'000 received from the proposal payload seems reasonable, given that acquiring 100'000 BAL is in the order of ~550'000 aUSDC.
- Anybody can call the `purchase()` function, passing as input the amount of BAL to sell. This will transfer the BAL from the purchaser to the Aave v2 Ethereum collector, and send the equivalent of aUSDC (or USDC) to the purchaser. Chainlink's price of USD/BAL is used on the calculations, and a 50 bps bonus is added to the amount of aUSDC/USDC to receive by the purchaser.
- The smart contract correctly enforces that the maximum amount to acquire is 100'000 BAL.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
