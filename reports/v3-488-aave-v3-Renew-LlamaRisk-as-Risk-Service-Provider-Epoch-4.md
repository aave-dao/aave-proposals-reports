# Proposal 488. Renew LlamaRisk as Risk Service Provider - Epoch 4

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=488)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-renew-llamarisk-as-risk-service-provider-epoch-4/24446)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x5F21aAeb5262aA11cf8b7CE2DC560773fFC06DDb)



## Certora Analysis

### Proposal Types
* :moneybag: :receipt: Asset transfers
* :bank: Payment stream

### Context
This AIP renews LlamaRisk as a Risk Service Provider for Aave for one year.

Aave’s risk layer recently lost critical infrastructure operated by a departing risk provider, including automated risk-oracle infrastructure, parameter automation pipelines, and Risk Steward coverage. LlamaRisk stepped in with Aave Labs to assume control of the Risk Steward and maintain operational continuity across Aave markets.

The immediate issue is continuity.

The structural issue is ensuring Aave does not depend on risk infrastructure the DAO cannot inspect, verify, or replace without disruption.

This renewal expands LlamaRisk’s scope across Aave V3, Aave V4, and Horizon, with a focus on protocol-owned risk infrastructure built on Chainlink CRE. This moves Aave’s risk layer toward infrastructure owned and controlled by the DAO, with off-chain logic independently verifiable through cryptographic workflow IDs.

LlamaRisk will deliver:

Protocol-owned risk infrastructure on Chainlink CRE.
Risk-managed price feeds for Pendle PTs, CAPO assets, USDe, RWA NAV, and related integrations.
Dynamic parameter automation for supply caps, borrow caps, interest rates, Umbrella calibration, credit lines, risk premiums, and liquidation configuration.
Safety mechanisms including freeze guardians and V4 per-Spoke circuit breakers.
Risk Steward co-ownership and operational accountability.
AIP and governance payload review.
Guardian signer duties.
Monitoring, dashboards, escalation playbooks, and incident response support.
Continued Horizon cooperation and LlamaGuard NAV expansion.
R&D for V4-native risk systems, including RWA liquidation infrastructure and instant settlement infrastructure.
Legal and regulatory research covering stablecoins, custody, counterparty risk, DeFi lending compliance, and tokenized RWA structuring.
LlamaRisk is currently a team of 16 contributors and expects to scale to 20+ contributors during this engagement. LlamaRisk also proposes to phase out remaining non-Aave work over six months and become Aave-exclusive by the midpoint of the engagement.

The approved compensation structure is:

| Component        |        Amount | Payment Method              |
| ---------------- | ------------: | --------------------------- |
| Upfront payment  | 1,500,000 GHO | Immediate payment           |
| Streamed payment | 1,500,000 GHO | Linear stream over one year |
| Streamed payment |    5,000 AAVE | Linear stream over one year |

The current GHO stream with ID 100071 will be terminated.


### Proposal Creation
Transaction: [0x702f505580a60d2769479788a9a40ca5667af378a0dc9a2177148167d77e43ff](https://etherscan.io/tx/0x702f505580a60d2769479788a9a40ca5667af378a0dc9a2177148167d77e43ff)
- `proposalId`: 488
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0x6d81dd9fc20a79167fa58571ee5738f5b745d21e4855cc42215e792fa537bef9

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 443,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x6d81dd9fc20a79167fa58571ee5738f5b745d21e4855cc42215e792fa537bef9",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/488.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/443.md)


### Technical Analysis

We have verified that the payload (action contract `0x5F21aAeb5262aA11cf8b7CE2DC560773fFC06DDb`) performs the following four actions against LlamaRisk's designated recipient address (`0x9eE16dBDE572886342fc1e2Db8525DEFB007b27c`):

1. **Cancellation of stream `100071`** on the Aave (EthereumLido) Collector (`0x464C71f6c2F760DdA6093dCB91C24c39e5d6e18c`), terminating the previous LlamaRisk engagement's GHO stream.

2. **Immediate transfer of 1,500,000 aGHO** (`AaveV3EthereumLidoAssets.GHO_A_TOKEN`, `0x18eFE565A5373f430e2F809b97De30335B3ad96A`) from the Aave (EthereumLido) Collector to LlamaRisk, corresponding to the upfront payment component.

3. **Creation of a new GHO stream** of 1,500,000 aGHO (`0x18eFE565A5373f430e2F809b97De30335B3ad96A`) over 365 days (`31,536,000` seconds), starting at `block.timestamp`, from the Aave (EthereumLido) Collector to LlamaRisk. This matches the streamed GHO component of the approved compensation.

4. **Creation of a new AAVE stream** from the Aave Ecosystem Reserve (`0x25F2226B597E8F9514B3F68F00f494cF4f286491`) to LlamaRisk, for `4,999,999,999,999,970,592,000` wei of AAVE (`0x7Fc66500c84A76Ad7e9c93437bFc5Ac33E2DDaE9`) over 365 days, starting at `block.timestamp`. The deposit is rounded down from the nominal 5,000 AAVE via integer truncation of the per-second rate (`floor(5000e18 / 31_536_000) * 31_536_000`); the shortfall is ~3×10⁻¹¹ AAVE, which is negligible.

We have verified that no other state is mutated by the payload.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.