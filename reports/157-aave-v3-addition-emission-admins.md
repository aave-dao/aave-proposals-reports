# Proposal 157. Aave v3 Ethereum/Optimism/Arbitrum - addition of EMISSION_ADMINs for LDO

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=157](https://app.aave.com/governance/proposal/?proposalId=157)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arfc-ldo-emission-admin-for-ethereum-arbitrum-and-optimism-v3-liquidity-pools/11478](https://governance.aave.com/t/arfc-ldo-emission-admin-for-ethereum-arbitrum-and-optimism-v3-liquidity-pools/11478)

<br>

## BGD analysis

<br>

### Proposal types

:link: :bridge_at_night: cross-chain execution

:gift: rewards

<br>

### Context

This proposal sets EMISSION_ADMIN roles for Lido to configure rewards of LDO on Aave v3 Ethereum, Optimism and Arbitrum.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0xc21cb8182cdb354f5aec5257b08239b5e3cc5579670b709d574739150512bf6a](https://etherscan.io/tx/0xc21cb8182cdb354f5aec5257b08239b5e3cc5579670b709d574739150512bf6a)

```
- id: 157
- creator: 0x55b16934c3661e1990939bc57322554d9b09f262
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x26366920975b24a89cd991a495d0d70cb8e1ba1f,0x5f5c02875a8e9b5a26fbd09040abcfdeb2aa6711,0x2e2b1f112c4d79a9d22464f0d345de9b792705f1]
- values: [0,0,0]
- signatures: [execute(),execute(address),execute(address)]
- calldatas: [0x,0x0000000000000000000000002cbf7856f51660aae066afababf9c854fa6bd11f,0x0000000000000000000000002cbf7856f51660aae066afababf9c854fa6bd11f]
- withDelegatecalls: [true,true,true]
- startBlock: 16650646
- endBlock: 16669846
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x414552595f91e1861b2864a4c18b6d0a0853e7ab285a263cff21dfc49e9f3798
```

<br>

### Aave Seatbelt report

**Ethereum report:**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/157.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/157.md)

**Optimism report:**

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/157_optimism_5_0.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/157_optimism_5_0.md)

**Arbitrum**

Aave Seatbelt doesn't support Arbitrum yet.

<br>

### Technical analysis

From a technical point of view, we have verified that the proposal correctly interacts both with Ethereum and the cross-chain governance system, executing the following actions:

1. [Ethereum payload](https://etherscan.io/address/0x26366920975b24a89cd991a495d0d70cb8e1ba1f#code)
  - Grant EMISSION_ADMIN role of LDO to Lido, on Aave v3 Ethereum.

2. [Optimism payload](https://optimistic.etherscan.io/address/0x2cbf7856f51660aae066afababf9c854fa6bd11f#code)
  - Grant EMISSION_ADMIN role of LDO to Lido, on Aave v3 Optimism.

3. [Arbitrum payload](https://arbiscan.io/address/0x2cbf7856f51660aae066afababf9c854fa6bd11f#code)
  - Grant EMISSION_ADMIN role of LDO to Lido, on Aave v3 Arbitrum.


<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: BGD reviewed the payload before the proposal was submitted.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD reviewed the procedure followed to submit the proposal.
