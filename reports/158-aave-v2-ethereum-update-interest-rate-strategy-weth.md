# Proposal 158. Aave v2 Ethereum - update WETH interest rate strategy

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=158](https://app.aave.com/governance/proposal/?proposalId=158)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-weth-wsteth-interest-rate-curve-ethereum-network/11372/6](https://governance.aave.com/t/arfc-weth-wsteth-interest-rate-curve-ethereum-network/11372/6)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the interest rate strategy for WETH on the Aave v2 Ethereum pool.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x5abb107e6ba59d8bb8f065334743a669041c9bcde06747fb8d36aa62008bca8f](https://etherscan.io/tx/0x5abb107e6ba59d8bb8f065334743a669041c9bcde06747fb8d36aa62008bca8f)

```
- id: 158
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xfb2a7eb134fa2d03d9a2c8fe0a9758132fe15357]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16650679
- endBlock: 16669879
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xb802e21e7ca82e5e4c49bd21e7d7c80d723bcd475b2fb9be1a4e2620e0da90c5
```

<br>

### Aave Seatbelt report

**IMPORTANT. The underlying Tenderly infrastructure used by Aave Seatbelt is creating problems at the moment in the tool, affecting reports generation. We have double checked everything even without the reports, and working in a solution**

[TBA]()

<br>

### Technical analysis

The proposal payloads do the following:
- Call the [Pool Configurator of Aave v2 Ethereum](https://etherscan.io/address/0x311Bb771e4F8952E6Da169b425E7e92d6Ac45756) to replace the current interest rate strategy of WETH with the one on deployed [HERE](https://etherscan.io/address/0xb8975328Aa52c00B9Ec1e11e518C4900f2e6C62a#code).
We verified that the only changes are on base variable borrow rate (from 0% to 1%) and variable slope 1 (from 5.75% to 3.8%).

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: Payload encoded via multiple targets and calldatas, no delegatecall

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the procedure followed to submit the proposal.
