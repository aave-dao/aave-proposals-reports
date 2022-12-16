# Proposal 131. Aave v2 Ethereum - update WETH interest rate strategy and reserve factor 

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=131](https://app.aave.com/governance/proposal/?proposalId=131)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-eth-interest-rate-curve-update/10580](https://governance.aave.com/t/arc-eth-interest-rate-curve-update/10580)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal changes the interest rate params of WETH on Aave v2 Ethereum, by replacing its current interest rate strategy contract with a new one. Additionally, it increases its Reserve Factor.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xca40aaa34d5f728e10b6f8971f124f39f5d0c575a467c1e3ee4b398cacd140cf](https://etherscan.io/tx/0xca40aaa34d5f728e10b6f8971f124f39f5d0c575a467c1e3ee4b398cacd140cf)

```
- id: 131
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x98bc9dfa3cecb37f1bdeadc6e774d39082756b19]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16183841
- endBlock: 16203041
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x78ce0d63ca0c186ca3f58e712d3f1861ced3dad15ce3ad4f0e005d1663b49caf
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/131.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/131.md)

**There seems to be some infrastructure problem on Tenderly, which causes the state transitions to show erroneously. We have double checked both payload code and events emitted, and everything seems correct**

<br>

### Technical analysis

We have verified that [the proposal's payload](https://etherscan.io/address/0x98bc9dfa3cecb37f1bdeadc6e774d39082756b19#code):
- Updates the interest rate strategy, with the new one properly changing the following params:
  - **Optimal utilisation point**: 70% -> 80%
  - **Variable slope 1**: 3% -> 5.75%
  - **Variable slope 2**: 100% -> 80%
  - **Stable slope 2**: 100% -> 80% 
- **Reserve Factor**: 10% -> 15%

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
