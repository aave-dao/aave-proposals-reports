# Proposal 109. Whitelist Balancer's liquidity mining claimer

<br>

### Voting link
[https://app.aave.com/governance/proposal/?proposalId=109](https://app.aave.com/governance/proposal/?proposalId=109)

<br>

### Governance forum discussion
[https://governance.aave.com/t/arc-whitelist-balancer-s-liquidity-mining-claim/9724](https://governance.aave.com/t/arc-whitelist-balancer-s-liquidity-mining-claim/9724)

<br>

## BGD analysis

<br>

### Proposal types

:handshake: partners

<br>

### Context
This proposal enables an smart contract to claim on behalf of the Balancer Linear Pool the stkAAVE accrued on the rewards program, previously active on Aave v2 Ethereum.

<br>

### Proposal creation
Transaction: [https://etherscan.io/tx/0xd13353329e6aa7b40d137807338c806d742081b0dfa325399d89d01262e7c0c8](https://etherscan.io/tx/0xd13353329e6aa7b40d137807338c806d742081b0dfa325399d89d01262e7c0c8)

```
- id: 109
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x9e0f13a2298a879c7834d84c2967fccc7fa42df8]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 15768988
- endBlock: 15788188
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x8e3b44d853e826373be20553b8ab937043dec6952f5014e12bdb2d37f483f7c4
```

<br>

### Technical analysis
We have verifier the proposal payload does the following:

1. Calls `setClaimer()` on the [Aave IncentivesController](https://etherscan.io/address/0xd784927Ff2f95ba542BfC824c8a8a98F3495f6b5), setting as claimer for the [Balancer Vault](https://etherscan.io/address/0xBA12222222228d8Ba445958a75a0704d566BF2C8) the previously deployed [claimer contract](https://etherscan.io/address/0x0e2d46fe246eb926d939A10efA96fB7d4EB14bB3).

The claimer contract (StkAaveRetrieval) allows only the Balancer Multisig to claim for itself the rewards accrued on the Aave IncentivesController, by interacting with static aDAI, static aUSDC and static aUSDT. 

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.

:white_check_mark: Only one payload used via delegatecall
