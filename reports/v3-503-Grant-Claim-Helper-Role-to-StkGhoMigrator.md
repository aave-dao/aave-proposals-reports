# Proposal 503. Grant Claim Helper Role to StkGhoMigrator

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=503)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-stkgho-sgho-migration-tool/25250)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x5bDfd799fe4951F7fa018a66834bf8F89b0c4fa5)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking


### Context
This proposal grants the `CLAIM_HELPER_ROLE` on the stkGHO Safety Module 👻 (`0x1a88Df1cFe15Af22B3c4c783D4e6F7F9e0C1885d`, `AaveSafetyModule.STK_GHO`) to the newly deployed **StkGhoMigrator** helper contract (`0xC836143e39201698e7d543bCf21AfF3415aE4697`). Authored by **Aave Labs** via the DAO-approved **direct-to-AIP** process (no Snapshot), it supports the stkGHO deprecation strategy by enabling one-click migration from the deprecated stkGHO token into the new ERC-4626 `sGHO` vault. Doing this manually requires four discrete steps (cooldown → redeem GHO → approve GHO → deposit into sGHO); the migrator bundles them into a single user-initiated `migrate()` call surfaced through the Aave UI. Forum: https://governance.aave.com/t/direct-to-aip-stkgho-sgho-migration-tool/25250.

### Proposal Creation
Transaction: [0xc2446a0479c085c2bfcc511c446abf6345060db0c1e8f46a660f4de30d89eca3](https://etherscan.io/tx/0xc2446a0479c085c2bfcc511c446abf6345060db0c1e8f46a660f4de30d89eca3)
- `proposalId`: 503
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0xeef38c97d29672d9c47d4a28909c3e17da75c23da35d67062633ce3598547ed9

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 454,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xeef38c97d29672d9c47d4a28909c3e17da75c23da35d67062633ce3598547ed9",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/503.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/454.md)


### Technical Analysis
1. `setPendingAdmin` runs in the short-executor delegatecall context, which is the current `CLAIM_HELPER_ROLE` admin (`EXECUTOR_LVL_1` `0x5300A1a1…`), satisfying `onlyRoleAdmin`.
2. `claimHelperRole()` has the migrator accept the pending role, becoming the sole `CLAIM_HELPER_ROLE` holder — completing the transfer atomically within the transaction.

- **Grantee:** `0xC836143e39201698e7d543bCf21AfF3415aE4697` — the StkGhoMigrator contract, verified **Exact Match** on Etherscan; absent from the address-book (deterministic Check 4: `1/1 not identified`, expected for a fresh helper) but byte-identical to the customer-review repo (Check 2: 2/2). Its constructor references match `GhoEthereum.GHO_TOKEN` (`0x40D16FC0…`) and `GhoEthereum.SGHO` (`0xE1753F2e…`).
- **Target:** `AaveSafetyModule.STK_GHO` == `0x1a88Df1c…`, matching the spec. `STK_GHO_MIGRATOR` is declared `constant` (Check 3 pass).
- **Role semantics:** `CLAIM_HELPER_ROLE` authorizes `redeemOnBehalf`, `cooldownOnBehalfOf`, and `claimRewardsAndRedeemOnBehalf` on stkGHO — required so the migrator can trigger cooldown and redeem a user's stkGHO without the standard wait, then deposit the resulting GHO into sGHO.
- **Seatbelt:** confirms `_admins[CLAIM_HELPER_ROLE=2]` moving from the Executor 👻 `0x5300a1a1…` to the migrator, with `PendingAdminChanged` and `RoleClaimed` emitted and no `selfdestruct`. It flags one unverified contract `0xD73a92Be…` in the call path (not the grantee) that should be confirmed as a recognized Aave component before approval.

The `test_e2e_migration` test stakes 100 GHO, executes the payload, calls `migrate()`, and verifies the user's stkGHO goes to 0, the migrator retains no GHO, and the received sGHO shares redeem back to the original principal (±1 wei). The on-chain code faithfully implements the stated intention.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.