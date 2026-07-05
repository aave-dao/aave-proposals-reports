# Proposal 499. Update USDG Price Feed on Aave V3 Instances

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=499)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/technical-maintenance-proposals/15274/132)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xe9429477780D46D429668B12c1E27202854481bb)

* Xlayer - [proposal payloads](https://www.oklink.com/xlayer/address/0xd7f2ff8675d7f11f57542c74456c80dabfa4ac04)



## Certora Analysis

### Proposal Types
* :wrench: :bar_chart: Configuration updates


### Context

Proposal 499 ("Update USDG Price Feed on Aave V3 Instances") migrates the `USDG` price source on the DAO-controlled Aave V3 **Ethereum Core** and **X Layer** instances from the legacy fixed 1.0 oracle to a newly deployed **PriceCapAdapterStable (CAPO)**. Per [LlamaRisk's assessment](https://governance.aave.com/t/technical-maintenance-proposals/15274/132), USDG liquidity has improved such that the Chainlink USDG/USD feed now offers higher-quality pricing than the incumbent source; the proposal wraps that Chainlink feed in an adapter capped at **1.04** (tracks Chainlink, bounded on the upside). On Ethereum the same adapter is also assigned to **PT-USDG-28MAY2026**, which has matured (28-May-2026, past today's 05-Jul-2026) and redeems 1:1 to USDG. Proposal 499 bundles two payloads — Ethereum (payload 452) and XLayer (payload 6). The Ink whitelabel instance mentioned on the forum is handled separately via its permissioned payloads controller and is **not** part of this governance proposal.

### Proposal Creation
Transaction: [0x2e360b200dbd49cbc1e3e1c2c943a1a051bbfe60aabf8d5f2b00e834c9062c10](https://etherscan.io/tx/0x2e360b200dbd49cbc1e3e1c2c943a1a051bbfe60aabf8d5f2b00e834c9062c10)
- `proposalId`: 499
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0x1e366204a2c8767b4791062ed358dd55445dd5b0423f31245d37595e72866328

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 452,
        },
        {
            chain: "196",
            payloads_controller: "0x80e11cB895a23C901a990239E5534054C66476B5",
            payload_id: 6,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x1e366204a2c8767b4791062ed358dd55445dd5b0423f31245d37595e72866328",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/499.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/452.md)

* Xlayer - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/196/0x80e11cB895a23C901a990239E5534054C66476B5/6.md)


### Technical Analysis

Both payloads inherit `AaveV3Payload<Chain>` and effect the change purely through the config engine's `priceFeedsUpdates()` — no direct `poolConfigurator`/oracle calls, no stateful storage, one constant feed address each. The engine's `PriceFeedEngine._setPriceFeeds` validates each entry (`priceFeed != 0`, `latestAnswer() > 0`, `decimals() == 8`) before calling `AaveOracle.setAssetSources`.

**Ethereum** (`AaveV3Ethereum_UpdateUSDGPriceFeed_20260514.sol:15-38`, 👻 config engine) — two updates, both to CAPO `0x83D20dEEdcd4aC1313496c8CBcAad0fa298c0CE4`:
- `USDG_UNDERLYING` (0xe343...491D): `0xf29b1e...` (Fixed 1.0) → CAPO (Capped, ~0.9998)
- `PT_USDG_28MAY2026_UNDERLYING` (0x9db3...0548): `0x90498d...` (Fixed 1.0) → same CAPO (comment: "has matured and redeems 1:1 to USDG")

Tests confirm `decimals()==8`, `ASSET_TO_USD_AGGREGATOR()==0x14f0737d6b705259e521EA6E9E3506AC78dBd311` (Chainlink USDG/USD), `getPriceCap()==1.04e8`, `isCapped()==false` at par, `0.98e8 < price ≤ cap`, oracle price == CAPO answer, and matured PT-USDG prices 1:1 with USDG. The Seatbelt report shows both assets' source changed to `Capped USDG / USD` (latestAnswer 0.9998, 8 decimals), no `selfdestruct`, no unexpected state.

**X Layer** (`AaveV3XLayer_UpdateUSDGPriceFeed_20260514.sol:15-31`) — one update: `USDG_UNDERLYING` (0x4ae4...2dc8) → CAPO `0xe00B2732396a1f047d4A00e0165025A9cF400245`, sourcing Chainlink `0x385C6bDDE06b0E438319bF4ddBfFe51C521ABf3D`, cap 1.04, decimals 8. Seatbelt payload 6 confirms the single source change.

All addresses, Chainlink sources and the 1.04 cap match the IPFS spec (`UpdateUSDGPriceFeed.md`) byte-for-byte. The deterministic diff verified the Ethereum payload against the source-of-truth repo; the only explicit address flagged "unidentified" (0x83D2...) is the expected custom CAPO wrapper, whose Chainlink leg was drilled down and confirmed. **Caveat:** the XLayer payload (0xd7f2ff86...ac04) is **not verified on the OKLink explorer**, so no byte-level on-chain comparison is possible there — integrity on XLayer rests on the Seatbelt trace and the identical Ethereum sibling.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.