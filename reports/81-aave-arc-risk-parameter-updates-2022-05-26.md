# Proposal 81. Aave Arc - Risk Parameter Updates 2022/05/26

<br>

### Voting link
[https://app.aave.com/governance/proposal/?proposalId=81](https://app.aave.com/governance/proposal/?proposalId=81)

### Governance forum discussion
**Only the Aave Arc part of the discussion**
[https://governance.aave.com/t/arc-risk-parameter-updates-for-aave-v2-and-aave-arc-fireblocks-2022-05-26/8299](https://governance.aave.com/t/arc-risk-parameter-updates-for-aave-v2-and-aave-arc-fireblocks-2022-05-26/8299)

<br>

## BGD analysis

### Proposal types

:wrench: :bar_chart: params-update

:shinto_shrine: Aave Arc

### Context
This proposal queues on the Arc timelock an update of risk parameters for USDC on Aave Arc.

### Proposal creation
Transaction: [https://etherscan.io/tx/0x52c214382696a61db9390add8c451ae554f8fd602b5c378125616b0469ff1a72](https://etherscan.io/tx/0x52c214382696a61db9390add8c451ae554f8fd602b5c378125616b0469ff1a72)
```
- id: 81
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xace1d11d836cb3f51ef658fd4d353ffb3c301218]
- values: [0]
- signatures: []
- calldatas: [0xd9a4cbdf00000000000000000000000000000000000000000000000000000000000000a000000000000000000000000000000000000000000000000000000000000000e000000000000000000000000000000000000000000000000000000000000001200000000000000000000000000000000000000000000000000000000000000180000000000000000000000000000000000000000000000000000000000000028000000000000000000000000000000000000000000000000000000000000000010000000000000000000000004e1c7865e7be78a7748724fa0409e88dc14e67aa000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000847c4e560b000000000000000000000000a0b86991c6218b36c1d19d4a2e9eb0ce3606eb48000000000000000000000000000000000000000000000000000000000000222e000000000000000000000000000000000000000000000000000000000000232800000000000000000000000000000000000000000000000000000000000028d20000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000]
- withDelegatecalls: [false]
- startBlock: 14923384
- endBlock: 14942584
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x79e335f8a7d839d481743a9e04132d856c6d6b92655666413237eaa5f38b6526
```

### Aave Seatbelt report
[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/081.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/081.md)

### Technical analysis
From a technical perspective, we have verified that the calldata submitted as payload of the proposal does the following on Aave Arc, by queueing the action on the [ArcTimelock contract](https://etherscan.io/address/0xAce1d11d836cb3F51Ef658FD4D353fFb3c301218):

1. Calls `configureReserveAsCollateral()` on the [Arc Aave Pool Configurator](https://etherscan.io/address/0x4e1c7865e7be78a7748724fa0409e88dc14e67aa#code) for USDC, to set LTV to 87.5%, Liquidation Threshold to 90% and Liquidation Bonus to 4.5% (not modified).


### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: Payload encoded via multiple targets and calldatas, no delegatecall

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the payload before the proposal was submitted.

:x: BGD reviewed the procedure followed to submit the proposal.
