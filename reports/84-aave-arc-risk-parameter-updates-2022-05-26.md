# Proposal 84. Aave Arc - Risk Parameter Updates 2022/05/26

<br>

### Voting link
[https://app.aave.com/governance/proposal/?proposalId=84](https://app.aave.com/governance/proposal/?proposalId=84)

### Governance forum discussion
**Only the Aave Arc part of the discussion**
[https://governance.aave.com/t/arc-risk-parameter-updates-for-aave-v2-and-aave-arc-fireblocks-2022-05-26/8299](https://governance.aave.com/t/arc-risk-parameter-updates-for-aave-v2-and-aave-arc-fireblocks-2022-05-26/8299)

<br>

## BGD analysis

### Proposal types

:wrench: :bar_chart: params-update

:shinto_shrine: Aave Arc

### Context

**This proposal is a repetition of proposal 81, on which YES won, but didn't reach enough quorum**

This proposal queues on the Arc timelock an update of risk parameters for USDC on Aave Arc.

### Proposal creation
Transaction: [https://etherscan.io/tx/0xb00c1ff320697c20c78c124426f44d70c1ecf8bd5c59b6fd96d7c8f7d51391a1](https://etherscan.io/tx/0xb00c1ff320697c20c78c124426f44d70c1ecf8bd5c59b6fd96d7c8f7d51391a1)
```
- id: 84
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xace1d11d836cb3f51ef658fd4d353ffb3c301218]
- values: [0]
- signatures: []
- calldatas: [0xd9a4cbdf00000000000000000000000000000000000000000000000000000000000000a000000000000000000000000000000000000000000000000000000000000000e000000000000000000000000000000000000000000000000000000000000001200000000000000000000000000000000000000000000000000000000000000180000000000000000000000000000000000000000000000000000000000000028000000000000000000000000000000000000000000000000000000000000000010000000000000000000000004e1c7865e7be78a7748724fa0409e88dc14e67aa000000000000000000000000000000000000000000000000000000000000000100000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000001000000000000000000000000000000000000000000000000000000000000002000000000000000000000000000000000000000000000000000000000000000847c4e560b000000000000000000000000a0b86991c6218b36c1d19d4a2e9eb0ce3606eb48000000000000000000000000000000000000000000000000000000000000222e000000000000000000000000000000000000000000000000000000000000232800000000000000000000000000000000000000000000000000000000000028d20000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000010000000000000000000000000000000000000000000000000000000000000000]
- withDelegatecalls: [false]
- startBlock: 15005807
- endBlock: 15025007
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x2d900e4177145ded5595790def76a02e744d61a17b70b54501819744ba85d88e
```

### Aave Seatbelt report
[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/084.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/084.md)

### Technical analysis
From a technical perspective, we have verified that the calldata submitted as payload of the proposal does the following on Aave Arc, by queueing the action on the [ArcTimelock contract](https://etherscan.io/address/0xAce1d11d836cb3F51Ef658FD4D353fFb3c301218):

1. Calls `configureReserveAsCollateral()` on the [Arc Aave Pool Configurator](https://etherscan.io/address/0x4e1c7865e7be78a7748724fa0409e88dc14e67aa#code) for USDC, to set LTV to 87.5%, Liquidation Threshold to 90% and Liquidation Bonus to 4.5% (not modified).


### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: Payload encoded via multiple targets and calldatas, no delegatecall

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the payload before the proposal was submitted.

:x: BGD reviewed the procedure followed to submit the proposal.
