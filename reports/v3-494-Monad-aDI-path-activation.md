# Proposal 494. Monad aDI path activation

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=494)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/technical-maintenance-proposals/15274/130)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x5c67Ac24Ed23B343d26E9D6AC682ce34617ae634)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates

### Context
Proposal 494 — **Monad a.DI path activation** — wires the Aave Delivery Infrastructure (a.DI) governance messaging path from Ethereum to Monad (chainId 143). Proposed by Aave Labs (forum [post #130](https://governance.aave.com/t/technical-maintenance-proposals/15274/130), "a.DI/Governance. Enable support for Monad"; [voting page](https://vote.onaave.com/proposal/?proposalId=494)), it registers the three pre-deployed Monad governance bridge adapters — Chainlink CCIP, Hyperlane, and LayerZero — on the canonical Ethereum `CrossChainController` 👻 (`0xEd42a7D8559a463722Ca4beD50E0Cc05a386b0e1`) forwarder, so DAO governance payloads can be relayed to the forthcoming Monad deployment. It is part of the broader Monad onboarding and follows the trusted SP direct-to-AIP maintenance track. A single Ethereum payload (PayloadsController id 447, `0x5c67Ac24Ed23B343d26E9D6AC682ce34617ae634`), created by `0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF` at access level 1, is the only on-chain action.

### Proposal Creation
Transaction: [0x98c808966ab2ab8ec7cc81b989bd15f2c80a461dda0b27b4a4395c3864ea65d2](https://etherscan.io/tx/0x98c808966ab2ab8ec7cc81b989bd15f2c80a461dda0b27b4a4395c3864ea65d2)
- `proposalId`: 494
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0xae19ce301e3d7c467c34b7f3ceb201e3cf9efa6341de04c27e88ac8dca31d4e6

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 447,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xae19ce301e3d7c467c34b7f3ceb201e3cf9efa6341de04c27e88ac8dca31d4e6",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/494.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/447.md)


### Technical Analysis
The verified payload (`Ethereum_Monad_Path_Payload`, Etherscan **Exact Match**, Solidity v0.8.27) hard-codes the path configuration as immutables and, in `execute()`, mutates the Ethereum `CrossChainController` 👻 (`0xEd42a7D8559a463722Ca4beD50E0Cc05a386b0e1` = `GovernanceV3Ethereum.CROSS_CHAIN_CONTROLLER`) for **destination chain id 143 (Monad)**:

1. **Enable three forwarder bridge adapters** (current Ethereum adapter → destination Monad adapter):
   - CCIP `0x7c28CEb47b49cFAC40e718dD407e4249F9C891F6` → `0x7Cd4245433185A08084E9cf80300682397F733AC`
   - Hyperlane `0x6bda311748E6542d578b167d791A4130f3FbBc67` → `0xb8F8aFdB7f1F4Ca9D842adFF86d052cb0C9f20CA`
   - LayerZero `0xf9482751C9937fF940b93B5921B8984645dD0a53` → `0xb544322f8e59B71d7875e0E2EbceB7f3783257BE`
   All three match the forum spec 1:1.
2. **Set `optimalBandwidth = 2`** for chain 143 — forward via 2 of the 3 adapters by default (2-of-3 redundancy on the forwarder side).
3. **Increase the CrossChainController's LINK allowance** (`0x514910771AF9Ca656af840dff83E8264EcF986CA`) to a max-uint256 amount for a CCIP fee spender (~`0x80226fc0Ee2b096224EeAc085Bb9a8cba1146f7D`) so the CCIP adapter can pay message fees.

The Seatbelt report for payload 447 corroborates this: three `BridgeAdapterUpdated` events (consistent with a single, forwarder-side update — six would be expected if receivers were also updated here), `OptimalBandwidthUpdated(chainId: 143, bandwidth: 2)`, and the LINK approval; no `selfdestruct` and all touched contracts verified. The destination addresses are consistent with the Monad a.DI deployment (`GovernanceV3Monad.CROSS_CHAIN_CONTROLLER = 0x8dd5b84b26ae3916A5Fb34C8968F93d206216b63`). Deterministic check 3 confirms all globals are `constant`/`immutable`.

The on-chain code faithfully implements the stated intention for the Ethereum (forwarder) half of the path.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.