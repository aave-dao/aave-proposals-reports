# Proposal 265. Aave v3 Arbitrum - wstETH supply cap update

<br>


### Voting link

[https://app.aave.com/governance/proposal/?proposalId=265](https://app.aave.com/governance/proposal/?proposalId=265)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-chaos-labs-risk-stewards-increase-caps-reth-and-wsteth-on-v3-arbitrum/13817](https://governance.aave.com/t/arfc-chaos-labs-risk-stewards-increase-caps-reth-and-wsteth-on-v3-arbitrum/13817)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

<br>

### Context

This proposal updates the supply cap of wstETH on Aave v3 Arbitrum.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xc2fa31b277f5c1aad6fdf2010ffe41e754657a0662854e814f46be5526d8cedc](https://etherscan.io/tx/0xc2fa31b277f5c1aad6fdf2010ffe41e754657a0662854e814f46be5526d8cedc)

```
- id: 265
- creator: 0x329c54289ff5d6b7b7dae13592c6b1eda1543ed4
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0xd1b3e25fd7c8ae7caddc6f71b461b79cd4ddcfa3]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x000000000000000000000000134c50556de1a83dd947c9460a58d8d60a289cea]
- withDelegatecalls: [true]
- startBlock: 17635942
- endBlock: 17655142
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0xadc8fa84ad5b2a4a732872d60b266be51541101797f024b1e9442b21d8093d47
```

<br>

### Aave Seatbelt reports

**Ethereum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/265.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/265.md)

**Arbitrum**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/265_Arbitrum_pending_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/265_Arbitrum_pending_0.md)

<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system to communicate with Arbitrum.

From a technical perspective, we have verified the [proposal payload](https://arbiscan.io/address/0x134c50556de1a83dd947c9460a58d8d60a289cea#code#F1#L13) correctly uses the BGD's Aave Config Engine of Aave v3 Arbitrum, in this case, to update the supply cap of wstETH the following way:
- Supply cap: 18'750 wstETH -> **30'000 wstETH**

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
