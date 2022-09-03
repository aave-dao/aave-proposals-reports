# Proposal 97. Halt ETH borrowing on Aave v2 Ethereum

<br>

### Voting link

[https://app.aave.com/governance/proposal/?proposalId=97](https://app.aave.com/governance/proposal/?proposalId=97)

<br>

### Governance forum discussion

[https://governance.aave.com/t/arc-aave-ethpow-fork-risk-mitigation-plan/9438/3](https://governance.aave.com/t/arc-aave-ethpow-fork-risk-mitigation-plan/9438/3)

<br>

## BGD analysis

<br>

### Proposal types

:wrench: :bar_chart: params-update

:heavy_minus_sign: :ice_cube: halt-borrow

<br>

### Context

The proposal disables ETH borrowing (via WETH) on Aave v2 Ethereum, as a cautionary measure to avoid high utilisation, and consequently liquidation blockers, on the upcoming Ethereum Merge: the transition of the network to a Proof-of-Stake consensus mechanism.
In addition, the proposal releases 60 AAVE tokens from the Aave v2 Ethereum collector, to Maker DAO, who participated on the governance forum analysis.

<br>

### Proposal creation

Transaction: [https://etherscan.io/tx/0x25ca35f005aae409fc35bfc2be4edfc221d12fbb58ab47d0ad16f5aadb5ced85](https://etherscan.io/tx/0x25ca35f005aae409fc35bfc2be4edfc221d12fbb58ab47d0ad16f5aadb5ced85)

```
- id: 97
- creator: 0x683a4f9915d6216f73d6df50151725036bd26c02
- executor: 0xee56e2b3d491590b5b31738cc34d5232f378a8d5
- targets: [0x3d569673daa0575c936c7c67c4e6aeda69cc630c,0x311bb771e4f8952e6da169b425e7e92d6ac45756]
- values: [0,0]
- signatures: [,]
- calldatas: [0xf18d03cc00000000000000000000000025f2226b597e8f9514b3f68f00f494cf4f2864910000000000000000000000007fc66500c84a76ad7e9c93437bfc5ac33e2ddae9000000000000000000000000be8e3e3618f7474f8cb1d074a26affef007e98fb00000000000000000000000000000000000000000000000340aad21b3b700000,0xa8dc0f45000000000000000000000000c02aaa39b223fe8d0a0e5c4f27ead9083c756cc2]
- withDelegatecalls: [false,false]
- startBlock: 15461634
- endBlock: 15480834
- strategy: 0xb7e383ef9b1e9189fc0f71fb30af8aa14377429e
- ipfsHash: 0x1d008d832f4a2aef5eb81bf1ff8becbd6bc67e6405ec3921b984569389852b66
```

<br>

### Aave Seatbelt report

[https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/097.md](https://github.com/bgd-labs/seatbelt-for-ghosts/blob/main/reports/Aave/0xEC568fffba86c094cf06b22134B23074DFE2252c/097.md)


<br>

### Technical analysis

We have verified, that this proposal, as described on Snapshot and the Aave governance forum, does the following:
1. Call `transfer()` on the [controller of the Aave ecosystem's reserve](https://etherscan.io/address/0x3d569673daa0575c936c7c67c4e6aeda69cc630c#code), targeting the [Aave Ecosystem Reserve](https://etherscan.io/address/0x25f2226b597e8f9514b3f68f00f494cf4f286491), to transfer 60 AAVE tokens to [MakerDAO pause proxy contract](https://etherscan.io/address/0xbe8e3e3618f7474f8cb1d074a26affef007e98fb).
2. Call `disableBorrowingOnReserve()` for WETH on the [pool configurator of Aave v2 Ethereum](https://etherscan.io/address/0x311Bb771e4F8952E6Da169b425E7e92d6Ac45756).

It is important to highlight that this proposal doesn't act on any other Aave pool, which seems quite asymmetric.

<br>

### BGD validations

:white_check_mark: The code on the proposal payload corresponds to the proposal specification.

:white_check_mark: Payload encoded via multiple targets and calldatas, no delegatecall

:question: The proposal includes a proper tests suite, checking all necessary post-conditions.

:x: BGD reviewed the payload before the proposal was submitted.

:x: BGD reviewed the procedure followed to submit the proposal.
