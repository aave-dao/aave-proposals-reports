# Proposal 127. Aave <> StarkNet Phase I - Bridge activation

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=127](https://app.aave.com/governance/proposal/?proposalId=127)

<br>

### Governance forum discussion

[https://governance.aave.com/t/aave-starknet-phase-i-release/10428/5](https://governance.aave.com/t/aave-starknet-phase-i-release/10428/5)

<br>

## BGD analysis

<br>

### Proposal types

:link: :bridge_at_night: cross-chain execution

<br>

### Context

This proposal deploys and activates the Bridge smart contract for Aave v2 Ethereum aTokens from/to StarkNet.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xd638b0ea69ffd24094d62c64c6f8c30a44585a9edb629faf5ec0ff3eb8aa195d](https://etherscan.io/tx/0xd638b0ea69ffd24094d62c64c6f8c30a44585a9edb629faf5ec0ff3eb8aa195d)

```
- id: 127
- creator: 0xb85fa70cf9ab580580d437bdea785b71631a8a7c
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x4919e176f02142c20727da215e8dc1b3d046d026]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16089593
- endBlock: 16108793
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x19f26b6d93010714a86ce27a9e66d5a72f03eb5831b72993fcb622b6007c4d2c
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/127.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/127.md)

<br>

### Technical analysis

We have verified that from a technical perspective, the [proposal payload](https://etherscan.io/address/0x4919e176f02142c20727da215e8dc1b3d046d026#code) does what has been specified in the Aave governance forum and AIP description. More specifically, the actions executed are:

1. The proxy contract for the Bridge gets deployed deterministically, by using the Proxy Factory [HERE](https://etherscan.io/address/0xC354ce29aa85e864e55277eF47Fc6a92532Dd6Ca#code). The Aave governance Level 1 Executor (Short) is set as proxy admin, and the [Bridge implementation](https://etherscan.io/address/0x69F4057cC8A32bdE63c2d62724CE14Ed1aD4B93A#code) is connected.
2. In the same external call of 1), we have verified that the parameters passed to the `initialize()` function match what is expected if following the documentation and the [Bridge codebase](https://github.com/aave-starknet-project/aave-starknet-bridge/blob/main/contracts/l1/Bridge.sol#L53). This includes the Starknet's side of the Bridge, the StarkNet core bridge address on Ethereum, the Aave v2 Ethereum IncentivesController contract, and finally, the pair of L1/L2 aTokens for USDC/DAI/USDT, together with 30'000 deposit ceiling for each of them.
3. Finally, there is an external delegatecall to the Aave StarkNet forwarder contract, in order to pass a message to StarkNet and activate the system there.

We have verified that the addresses included on the payload match with the documentation on the repository of the project [HERE](https://github.com/aave-starknet-project/aave-starknet-bridge#deployed-contracts).


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
