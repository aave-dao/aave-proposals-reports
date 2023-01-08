# Proposal 140. Aave v3 Optimism - Update of AAVE supply cap

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=140](https://app.aave.com/governance/proposal/?proposalId=140)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-risk-parameter-updates-for-aave-v3-optimism-2022-12-29/11213](https://governance.aave.com/t/arc-risk-parameter-updates-for-aave-v3-optimism-2022-12-29/11213)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal is an update of the supply cap for the AAVE asset on Aave v3 Optimism, by Gauntlet.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xb333e1c1a0d14989880d46b59ccbda78ec8c3721a40edfd38586fcece91ac2b8](https://etherscan.io/tx/0xb333e1c1a0d14989880d46b59ccbda78ec8c3721a40edfd38586fcece91ac2b8)

```
- id: 140
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x00000000000000000000000031976dc2ea27e75cc5a3687ed594d17127f9b72e]
- withDelegatecalls: [true]
- startBlock: 16351665
- endBlock: 16370865
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xe06d5211b4f8b59decdb58811d73d40ed66a34842fa39597c946795e3752b83a
```

<br>

### Aave Seatbelt reports

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/140.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/140.md)


**Optimism**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/140_optimism_2_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/140_optimism_2_0.md)


<br>

### Technical analysis

From a technical perspective, we have verified that the proposal effectively goes through the cross-chain governance mechanism for Optimism, and its [payload on the destination chain](https://optimistic.etherscan.io/address/0x31976dc2ea27e75cc5a3687ed594d17127f9b72e#code) correctly calls the [Aave v3 Optimism PoolConfigurator](https://optimistic.etherscan.io/address/0x8145eddDf43f50276641b55bd3AD95944510021E) to update the AAVE supply cap to 100'000 AAVE.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
