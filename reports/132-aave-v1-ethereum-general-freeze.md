# Proposal 132. (REPETITION OF 129) Aave v1 Ethereum - freeze all assets

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=132](https://app.aave.com/governance/proposal/?proposalId=132)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-strategy-on-sunsetting-of-aave-v1/9450](https://governance.aave.com/t/arc-strategy-on-sunsetting-of-aave-v1/9450)

<br>

## BGD analysis

<br>

### Proposal types

:ice_cube: freeze-asset

<br>

### Context

This proposal freezes all assets for the Aave v1 and Aave v1 AMM pools, in order to progress with the sunset of v1 instances of the protocol.
Important to highlight that this is an exact repetition of proposal 129.


<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x814d141b540001855af4d3f01eb2fd4bef50c2569755a8b6e390207645bf0843](https://etherscan.io/tx/0x814d141b540001855af4d3f01eb2fd4bef50c2569755a8b6e390207645bf0843)

```
- id: 132
- creator: 0xf71fc92e2949ccf6a5fd369a0b402ba80bc61e02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x6f02253c80a041a773efa35c98d4bc14a0f6ef9e]
- values: [0]
- signatures: [execute()]
- calldatas: [0x]
- withDelegatecalls: [true]
- startBlock: 16225891
- endBlock: 16245091
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x02e04de8258c1dca9c4c6099d8ac2142f1f2833bad5a7ca4154a12aa8f4dd548
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/132.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/132.md)


<br>

### Technical analysis

This proposal has been created by BGD Labs, so we find more appropriate to describe what exactly the [payload](https://etherscan.io/address/0x6f02253c80a041a773efa35c98d4bc14a0f6ef9e#code) does:
1. Fetches the addresses of all listed assets on both the v1 and v1 AMM pools.
2. For each asset of each pool, call `freezeReserve()` on the respective Pool Configurator contract, fetched from each addressed provider.

In terms of security procedures, we have:
- Verified that addresses (pool addresses providers) are correct.
- Test in a Ethereum fork environment that, after simulating the execution of the payload, all assets are frozen, [HERE](https://github.com/bgd-labs/aave-proposal-freeze-v1/blob/master/tests/ProposalPayloadAaveFreezeV1.t.sol).
- Simulation the execution on a fork environment and checking on an [Aave v1 UI](https://app-v1.aave.com/) that effectively, the assets appear as frozen.

The proposal is really simple, so we don't consider any extra security review was necessary.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.

:white_check_mark: Only one payload used via delegatecall

:white_check_mark: BGD wrote the payload.

:x: With BGD writing the payload, at least another party reviewed it.
