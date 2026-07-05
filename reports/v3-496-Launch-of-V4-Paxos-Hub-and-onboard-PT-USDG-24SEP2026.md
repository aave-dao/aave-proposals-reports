# Proposal 496. Launch of V4 Paxos Hub and onboard PT-USDG-24SEP2026

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=496)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-onboard-pt-usdg-24sep2026-to-aave-v4-on-ethereum/24942/3)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xa10b9DdA31E3ACbB6C8F1E74F9a7504331a67757)

## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates

* :gem: :new: Listing new assets

## Context

Proposal 496 (direct-to-AIP, authored by Aave Labs; risk assessment by LlamaRisk) launches a new, isolated **Paxos Hub** on Aave V4 Ethereum (`0x62d6…0368`) and onboards **PT-USDG-24SEP2026** — the next rollover maturity in the USDG-backed Pendle PT series, succeeding the expired PT-USDG-28MAY2026 — as the sole collateral of a single new **USDG Pendle spoke** (`0x956d…a7f9`), a correlated-stablecoin market. PT-USDG is borrowable against USDC, USDT (supplied natively to the Paxos Hub) and USDG (drawn from the Core Hub via a cross-hub credit line). A dedicated hub provides risk isolation for USDG-correlated collateral while limiting Core-Hub exposure to the USDG credit line and its 30M draw cap.

The proposal also performs a **protocol-wide oracle change**: it migrates the **USDG price reference** from a fixed $1.00 feed to the live Chainlink USDG/USD feed (`0x14f0…d311`) wrapped in a `PriceCapAdapterStable` (`0x83D2…0CE4`) with a **1.04 upper cap**, applied to the USDG reserve on every existing spoke that used the fixed feed (Main, Forex, Gold) and the new spoke, and used as the base of the PT-USDG linear-discount oracle (`0x89F6…712e`).

A single payload (449, `0xa10b9DdA31E3ACbB6C8F1E74F9a7504331a67757`) executes everything: hub bring-up, three hub asset listings, four spoke reserve listings, four spoke asset cap configs, liquidation config, position-manager activation, AccessManager role wiring, a role grant to the L1 executor, and the USDG oracle repointing.

### Proposal Creation
Transaction: [0x1c8dcb67e843527cb08ae35a889876953a1d8394352c5bc15128039d28052873](https://etherscan.io/tx/0x1c8dcb67e843527cb08ae35a889876953a1d8394352c5bc15128039d28052873)
- `proposalId`: 496
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0x5b674a130e8424ebcdfde15fb4d6c09029eaf8f00f62fa99b981d78467497b45

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 449,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x5b674a130e8424ebcdfde15fb4d6c09029eaf8f00f62fa99b981d78467497b45",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/496.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/449.md)


## Technical Analysis

The payload `AaveV4Ethereum_OnboardPTUSDG24SEP2026OnV4PaxosUSDGPendle_20260514` inherits `AaveV4PayloadEthereumSpoke` (→ `AaveV4PayloadSpoke` → `AaveV4PayloadHub` → `AaveV4Payload`) and drives the V4 config engine through overrides:

- **New hub online** — `newHubs()` returns `[PAXOS_HUB]` (`0x62d6…0368`); `_hubTargetFunctionRoleUpdates()` wires its restricted selectors to HUB_CONFIGURATOR / HUB_FEE_MINTER / HUB_DEFICIT_ELIMINATOR roles on the shared AccessManager.
- **`_preExecute()`** grants `SPOKE_CONFIGURATOR_DOMAIN_ADMIN_ROLE` to `EXECUTOR_LVL_1` (delay 0) so the engine can configure the freshly-deployed spoke (the Seatbelt 'AaveV2 Pool Admin' label is just an alias for that executor address).
- **Hub asset listings (3)** — PT-USDG (liquidity fee 0, non-borrowable IR preset 99%/0/0/0, tokenization addCap 0), USDC and USDT (liquidity fee 10%, borrowable IR optimal 92% / slopes 4%/20% / base 0, tokenization addCap 13M each).
- **Spoke asset configs (4)** — PT-USDG add 15M / draw 0; USDC 13M/13M; USDT 13M/13M; USDG on the **Core Hub** add 0 / draw 30M (the cross-hub credit line). All active, none halted.
- **Spoke reserve listings (4)** — PT-USDG: collateral-only (`borrowable:false`), CF 94%, max liq bonus 103.20%, liq fee 10%, priced by `0x89F6…712e`. USDC/USDT: borrowable, CF 0, priced by the main-spoke feeds. USDG: borrowable, CF 0, `receiveSharesEnabled:false`, priced by the new USDG CAPO `0x83D2…0CE4`.
- **Liquidation config** — targetHF 1.0277e18, HF-for-max-bonus 0.99e18, bonus factor 1.0; the base helper also activates the four standard position managers (Giver, Taker, Config, SignatureGateway).
- **USDG oracle repointing** — `spokeReserveConfigUpdates()` sets `priceSource = USDG_PRICE_FEED` (KEEP_CURRENT everywhere else) for USDG on FOREX, GOLD and MAIN spokes.

The accompanying fork test suite pins every parameter above and additionally verifies the oracle adapters (Pendle linear-discount formula, par-at-maturity, zero-on-nonpositive-source; USDG CAPO sources Chainlink `0x14f0…d311`, decimals 8, 1.04 cap, legacy fixed feed `0xF29b…216d` removed everywhere, exactly 4 USDG reserves repriced) and exercises supply/borrow/liquidation/wrap-redeem end-to-end. The deterministic `ReviewDiffCheck` produced no diff (verified on-chain source equals reviewed repo source; the only DiffCheck output was expected v3-vs-v4 interface drift). **Verification limitation:** the `aave-v4` core source submodule was not checked out locally, so the config-engine `execute()` orchestration and the oracle implementations were validated via the helper bases and tests rather than re-audited from source.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.