# Proposal 497. TokenLogic Service Provider Renewal

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=497)

### Governance Forum Discussion
[Link to forum discussion](N/A)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x49246a072B3bDD942ABBa4e26a619121EddD05CE)

## Certora Analysis

### Proposal Types

* :bank: Payment stream

## Context

Proposal 497 — **TokenLogic Service Provider Renewal** (ARFC TokenLogic Phase II Extension), authored by @TokenLogic. It renews and expands TokenLogic's mandate as an Aave Service Provider and funds the next 12-month engagement; the existing KPI program is unchanged. Pre-approved on Snapshot and discussed on the governance forum, the single Ethereum payload re-bases TokenLogic's funding: it cancels the prior `aEthLidoGHO` stream, grants an additive GHO allowance to the TokenLogic multisig, and opens new `aEthLidoGHO` and `AAVE` vesting streams over 365 days to that multisig.

- Snapshot: https://snapshot.org/#/s:aavedao.eth/proposal/0x6c2814dc5da68698105894f1c450c80aa2296243ff737843cf9e869eecd8fa69
- Forum (ARFC): https://governance.aave.com/t/arfc-tokenlogic-phase-ii-extension/24846
- Beneficiary: TokenLogic multisig `0xAA088dfF3dcF619664094945028d44E779F19894` (2/4 Safe).

### Proposal Creation
Transaction: [0xfed1099d114a4e87886f51bc384572ffb62d604507605a120ca097f366737e99](https://etherscan.io/tx/0xfed1099d114a4e87886f51bc384572ffb62d604507605a120ca097f366737e99)
- `proposalId`: 497
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0xbc5c5e778840cae9948f7474cbf6d509e28c353768d7c84b999b6ebeaf232849

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 450,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xbc5c5e778840cae9948f7474cbf6d509e28c353768d7c84b999b6ebeaf232849",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/497.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/450.md)


### Technical Analysis

Single Ethereum payload 👻 `0x49246a072B3bDD942ABBa4e26a619121EddD05CE` (payload id 450 on PayloadsController 👻 `0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5`), contract `AaveV3EthereumLido_ARFCTokenLogicPhaseIIExtension_20260526`, executed via `delegatecall` from `execute()`. It inherits only `IProposalGenericExecutor` and declares only `constant` globals, and the verbatim verified Etherscan source matches the review-repo source line-for-line. It performs four actions, all directed to TokenLogic multisig `TOKEN_LOGIC = 0xAA088dfF3dcF619664094945028d44E779F19894`:

1. **Cancel prior stream** — `AaveV3EthereumLido.COLLECTOR.cancelStream(100072)` (the existing 2.5M aEthLidoGHO stream). Accrued-but-unclaimed funds (~156K GHO per Seatbelt) are paid to the recipient; the remainder returns to the Collector.
2. **GHO allowance top-up** — `COLLECTOR.approve(GHO_A_TOKEN, TOKEN_LOGIC, currentAllowance + 2_000_000e18)`. **Additive**: it reads the current allowance and adds 2,000,000 aEthLidoGHO, preserving any unclaimed balance.
3. **New GHO stream** — `CollectorUtils.stream(...)` for 2,500,000 aEthLidoGHO over 365 days from 👻 `AaveV3EthereumLido.COLLECTOR` (Seatbelt: stream 100086). `CollectorUtils.stream` rounds the deposit to `(amount/duration)*duration` (`CollectorUtils.sol:132`), so the on-chain deposit is the largest multiple of 365 days ≤ 2.5M (negligible dust; tests assert within 0.001%).
4. **New AAVE stream** — `AAVE_ECOSYSTEM_RESERVE_CONTROLLER.createStream(ECOSYSTEM_RESERVE, TOKEN_LOGIC, (5_000e18/365 days)*365 days, AAVE, now, now+365 days)` (Seatbelt: stream 100019). The explicit `(amount/duration)*duration` floors the deposit to a multiple of the duration to satisfy the controller's divisibility requirement and avoid revert.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.