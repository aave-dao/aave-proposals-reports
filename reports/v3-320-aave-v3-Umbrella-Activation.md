# Proposal 320. Aave Umbrella Activation

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=320)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-aave-umbrella-activation/21521)

### Payloads

* Ethereum Umbrella Activation - [proposal payloads](https://etherscan.io/address/0x791DFc171F7ea6CAfD90C81F0E22f8814dB5d40e)

* Ethereum Legacy stk tokens adjustment - [proposal payloads](https://etherscan.io/address/0x974b06b64BDFdE598Ffc406026b15A27a1549C04)

* Ethereum Robot activation - [proposal payloads](https://etherscan.io/address/0x8E8Cb277F3eccF35Bdaed9C55b88Ce4318C75cc9)



## Certora Analysis

### Proposal Types

* :scroll: :small_red_triangle: Contract upgrades


### Context
This payload activates the `Umbrella` system, introducing new staking tokens tailored for Aave’s risk management needs, along with their reward and slashing configurations. It also includes adjustments to the legacy Safety Module to ensure a smooth transition and continued protocol coverage.

### Proposal Creation
Transaction: [0xcb3a29628f3cf5a441a167277fca54462ea58efa963cdddaf3f1aaa87dba6cb0](https://etherscan.io/tx/0xcb3a29628f3cf5a441a167277fca54462ea58efa963cdddaf3f1aaa87dba6cb0)
- `proposalId`: 320
- `creator`: 0xf71fc92e2949ccF6A5Fd369a0b402ba80Bc61E02
- `accessLevel`: 1
- `ipfsHash`: 0xddf05486e23c698eca87a9c111489f0a1af313021c6bacaa0dedc2982566e6dd

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 295,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xddf05486e23c698eca87a9c111489f0a1af313021c6bacaa0dedc2982566e6dd",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/320.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/295.md)


### Technical Analysis
- **Contract Registration & Deficit Elimination**  
  Verified that the `Umbrella` contract is properly registered in the `PoolAddressesProvider`, and that deficit elimination for USDC, USDT, WETH, and GHO is correctly implemented. We ensured that deficit amounts are accurately calculated, funds are transferred from the `Collector` to the `Executor`, and the elimination logic functions on-chain as intended.

- **StataToken & stk Token Integration**  
  Confirmed that each new `stk` token (e.g., `stkwaWETH.V1`) wraps the correct `StataToken` (ERC-4626), and that `previewDeposit(1e18)` is used to correctly compute the conversion from underlying to shares for `targetLiquidity`.

- **Reward Configuration**  
  Reviewed all `maxEmissionPerSecond` and `targetLiquidity` parameters for correctness, and validated that reward funding via `Collector` allowances covers exactly 180 days of emissions. Also checked that `distributionEnd` is set to one year from execution.

- **Slashing Configuration & Role Assignments**  
  Ensured slashing parameters (e.g., `deficitOffset`, `liquidationFee`) match the proposal. Verified that `REWARDS_ADMIN_ROLE` and `COVERAGE_MANAGER_ROLE` are granted to the correct entities (e.g., `PERMISSIONED_PAYLOADS_CONTROLLER_EXECUTOR`, `DEFICIT_OFFSET_CLINIC_STEWARD`).

- **Legacy stk Token Adjustments**  
  Confirmed emission reductions and `maxSlashablePercentage` updates for `stkAAVE`, `stkBPT`, and `stkGHO`. Verified that reward emissions for `stkGHO` are set to zero and the cooldown window is reduced to allow immediate unstaking.

- **Robot Deployment**  
  Validated the setup of `SlashingRobot` and `UmbrellaPPCRobot`: registration in `AAVE_CL_ROBOT_OPERATOR`, gas limit settings (`5_000_000`), and LINK funding flow. Ensured these robots are positioned to automate slashing checks and post-coverage updates.

We made sure that all parameters, permissions, and flows are implemented exactly as specified in the governance proposal and that the system transition from the Safety Module to Umbrella is secure, complete, and operationally sound.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.