# Proposal 498. Gho Monad Activation

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=498)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-deploy-aave-protocol-on-monad/24943)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xAcA69879963fFdb8873387772Be030c155D86fA0)

* Avalanche - [proposal payloads](https://snowtrace.io/address/0x127be8D9A305f5f6e91f6ae0CaE5C3572A6828A2)

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0x0ca6270a0fEd61298b24a74C885aA9A252Ce1Da6)

* Base - [proposal payloads](https://basescan.org/address/0x8c2984492015B38781F4b3908639b62a9c916aDA)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0xfffEAf725f29c90135E8AfeD1128Aca2238AFF72)

* Mantle - [proposal payloads](https://mantlescan.xyz/address/0x224778bDa0A90F9419E555B50Caf4895ebb4E5CE)

* Plasma - [proposal payloads](https://plasmascan.to/address/0x471db882ae609a77d2ebc7394b03ed6ac115c700)

* Xlayer - [proposal payloads](https://www.oklink.com/xlayer/address/0x4407972616ba026d47da8f9cb97fd7ae905ab707)


## Certora Analysis

### Proposal Types
* :scroll: :small_red_triangle: Contract upgrades

* :handshake: Permission granting and revoking


### Voting link
[Vote](https://vote.onaave.com/proposal/?proposalId=498)

### Governance forum discussion
[ARFC: Deploy Aave Protocol on Monad](https://governance.aave.com/t/arfc-deploy-aave-protocol-on-monad/24943) · [Snapshot](https://snapshot.box/#/s:aavedao.eth/proposal/0x24f105bd023c476a9b85fa87ff795bfeec769fa799ce6ada8e2724c9738049f6)

## Certora analysis

### Proposal types
* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates (cross-chain CCIP + GHO facilitator mechanic)

### Context
Authored by **@TokenLogic** (recognized Service Provider) and approved on Snapshot, this AIP activates GHO on **Monad** by wiring Chainlink CCIP lanes between Monad and the nine chains where GHO already lives (Ethereum, Arbitrum, Base, Avalanche, Gnosis, Ink, Plasma, Mantle, X-Layer). Each lane is configured bidirectionally with a **1,500,000 GHO** bucket capacity and a **300 GHO/second** refill. On Monad, the new CCIP TokenPool 👻 is registered as a GHO facilitator with a **100,000,000 GHO** bucket, and the GHO stewards (Aave-core / bucket / CCIP) are granted their respective privileged roles. It is a **10-payload cross-chain proposal** (one payload per chain) relayed through a.DI, with the Monad payload performing the full launch and the other nine each adding the single Monad lane. Per the forum thread, GHO lanes on Monad are contingent on Chainlink's CCIP v1.5→v1.6 upgrade; the goal is to establish GHO as a foundational stablecoin on Monad from launch.

### Proposal Creation
Transaction: [0x7544f5ee22679b96b755f250b7a5908442ec9489d2fb33f4b82b1cfab77d6086](https://etherscan.io/tx/0x7544f5ee22679b96b755f250b7a5908442ec9489d2fb33f4b82b1cfab77d6086)
- `proposalId`: 498
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0x32b046d88008819529d14f8ba0aabc84c6e393d89b2eac04232e2f9feb5cdf9c

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 451,
        },
        {
            chain: "43114",
            payloads_controller: "0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80",
            payload_id: 117,
        },
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 130,
        },
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 110,
        },
        {
            chain: "100",
            payloads_controller: "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
            payload_id: 78,
        },
        {
            chain: "57073",
            payloads_controller: "0x44D73D7C4b2f98F426Bf8B5e87628d9eE38ef0Cf",
            payload_id: 5,
        },
        {
            chain: "5000",
            payloads_controller: "0xF089f77173A3009A98c45f49D547BF714A7B1e01",
            payload_id: 8,
        },
        {
            chain: "9745",
            payloads_controller: "0xe76EB348E65eF163d85ce282125FF5a7F5712A1d",
            payload_id: 31,
        },
        {
            chain: "196",
            payloads_controller: "0x80e11cB895a23C901a990239E5534054C66476B5",
            payload_id: 5,
        },
        {
            chain: "143",
            payloads_controller: "0x442CA936e5E6Db875357d0A16481145c96dd9a82",
            payload_id: 0,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x32b046d88008819529d14f8ba0aabc84c6e393d89b2eac04232e2f9feb5cdf9c",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/498.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/451.md)

* Avalanche - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/43114/0x1140CB7CAfAcC745771C2Ea31e7B5C653c5d0B80/117.md)

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/130.md)

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/110.md)

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/78.md)

* Mantle - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/5000/0xF089f77173A3009A98c45f49D547BF714A7B1e01/8.md)

* Plasma - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/31.md)

* Xlayer - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/196/0x80e11cB895a23C901a990239E5534054C66476B5/5.md)


### Technical Analysis

**Architecture.** The Monad payload `AaveV3Monad_GhoMonadActivation_20260518` inherits `AaveV3GHOLaunch` (which extends `AaveV3GHOLane` and implements `IProposalGenericExecutor`). Its `execute()` (`AaveV3GHOLaunch.sol:51-57`) runs, in order: `acceptAdminRole(GHO)` on the TokenAdminRegistry; `acceptOwnership()` on the CCIP TokenPool 👻; grants `FACILITATOR_MANAGER_ROLE` + `BUCKET_MANAGER_ROLE` to the L1 executor; `addFacilitator(TOKEN_POOL, 'CCIP TokenPool v1.5.1', 100M)`; grants `RISK_ADMIN_ROLE` to GhoAaveCoreSteward; grants `BUCKET_MANAGER_ROLE` to GhoBucketSteward and registers the pool as a controlled facilitator; sets GhoCcipSteward as the pool's `rateLimitAdmin`; `applyChainUpdates` for all 9 remote chains; and finally `setPool(GHO, pool)` in the registry. Each of the nine remote payloads inherits `AaveV3GHOLane` and overrides `lanesToAdd()` to return exactly the Monad lane: `_asArray(_asChainUpdateWithDefaultRateLimiterConfig(GhoCCIPChains.MONAD()))`.

**Parameters (code → spec).**
- Lane rate limiter: `DEFAULT_RATE_LIMITER_CAPACITY = 1_500_000e18`, `DEFAULT_RATE_LIMITER_RATE = 300e18` (`AaveV3GHOLane.sol:15-16`), applied identically to inbound and outbound via `_asChainUpdateWithDefaultRateLimiterConfig`. Matches spec §1 / forum '1.5M / 300 GHO/sec'.
- Facilitator bucket: `DEFAULT_CCIP_BUCKET_CAPACITY = 100_000_000e18` (`AaveV3GHOLaunch.sol:31`). Matches `GhoMonadActivation.md:39` ('100,000,000 units') and forum '100M GHO'.
- Monad addresses in `GhoCCIPChains.MONAD()` (`GhoCCIPChains.sol:388-404`) equal the spec table (`GhoMonadActivation.md:33-37`): GhoToken `0xfc421aD3…`, TokenPool `0xA5AE05b7…`, BucketSteward `0xDe653901…`, CcipSteward `0x360d8aa8…`, AaveCoreSteward `0xA5Ba2138…`.

**Simulated storage diff (Monad payload).** Reproduces the intended effects exactly: `PoolSet(GHO, 0x0→0xA5AE05…)` and `AdministratorTransferred` on registry `0x11ACd984…`; `OwnershipTransferred` + `RateLimitAdminSet(0x360d8aa8…)` on the pool; `FacilitatorAdded(0xA5AE05…, 100000000000000000000000000)`; FACILITATOR_MANAGER + BUCKET_MANAGER to executor `0xa9d0EAFF…`, BUCKET_MANAGER to bucket steward `0xDe6539…`, and RISK_ADMIN (`0x8aa855a9…`) to `0xA5Ba2138…` on ACL_MANAGER `0xa9fEE192…`. Nine `ChainAdded` events cover the selectors for Ethereum/Arbitrum/Base/Avalanche/Gnosis/Ink/Plasma/Mantle/X-Layer, each with `capacity 1500000000000000000000000, rate 300000000000000000000` inbound and outbound; remoteToken values match real GHO deployments (Ethereum `0x40D16FC0…`, Arbitrum `0x7dfF7269…`, Base `0x6Bb7a212…`).

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.
