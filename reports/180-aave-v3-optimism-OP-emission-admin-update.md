# Proposal 180. Aave v3 Optimism - update EMISSION_ADMIN role for OP

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=180](https://app.aave.com/governance/proposal/?proposalId=180)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-grant-op-emission-admin-for-optimism-v3-liquidity-pool-to-lido-dao/11905](https://governance.aave.com/t/arfc-grant-op-emission-admin-for-optimism-v3-liquidity-pool-to-lido-dao/11905)

<br>

## BGD analysis

<br>

### Proposal types

:gift: rewards

<br>

### Context

This proposal sets EMISSION_ADMIN role for Lido to configure rewards of OP on Aave v3 Optimism, replacing the Optimism team.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xefb2af224d51650ee3b6ac0f4b5dce6b85cbe0cc2cfe249f39101e0f35467e96](https://etherscan.io/tx/0xefb2af224d51650ee3b6ac0f4b5dce6b85cbe0cc2cfe249f39101e0f35467e96)

```
- id: 180
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711]
- values: [0]
- signatures: [execute(address)]
- calldatas: [0x0000000000000000000000004b8d3277d49e114c8f2d6e0b2ed310e29226fe16]
- withDelegatecalls: [true]
- startBlock: 16841707
- endBlock: 16860907
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x81fd0481eb4a61b19e35127e22f5da5b58d8aca66cb633fc2212d23603c9e829
```

<br>

### Aave Seatbelt report

**Ethereum report:**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/180.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/180.md)

**Optimism report:**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/180_optimism_8_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/180_optimism_8_0.md)


<br>

### Technical analysis

We have verified the proposal uses correctly the Aave cross-chain governance system.

The [proposal payload](https://optimistic.etherscan.io/address/0x4b8d3277d49e114c8f2d6e0b2ed310e29226fe16#code#F21#L1) correctly interacts with the [EmissionManager of Aave v3 Optimism](https://optimistic.etherscan.io/address/0x048f2228D7Bf6776f99aB50cB1b1eaB4D1d4cA73) to set the `EMISSION_ADMIN` role to the [Gnosis Safe](https://optimistic.etherscan.io/address/0x5033823f27c5f977707b58f0351adcd732c955dd), by calling `setEmissionAdmin()`.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
