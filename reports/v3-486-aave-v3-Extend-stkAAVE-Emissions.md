# Proposal 486. Extend stkAAVE Emissions

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=486)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-amend-safety-module-emissions/16640/52)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x5acc174322235e6f4296E2e91F02d45775d4041D)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates
* :bank: Payment stream

### Context
Increase the AAVE allowance for the Safety Module stkAAVE to extend rewards distribution by 90 days while keeping the current emission rate unchanged.

### Proposal Creation
Transaction: [0x3ce356cfc57b4b7b5c53f5fd247134a22c58681503f59423dfe4fcd1f323f846](https://etherscan.io/tx/0x3ce356cfc57b4b7b5c53f5fd247134a22c58681503f59423dfe4fcd1f323f846)
- `proposalId`: 486
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0xc378d6152053431740328367b9a1cf8a141afa40797fef28ad8b2978592d3624

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 440,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xc378d6152053431740328367b9a1cf8a141afa40797fef28ad8b2978592d3624",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/486.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/440.md)


### Technical Analysis

* We have verified that the payload's logic matches the AIP specification (IPFS `0xc378d61520…592d3624`): it reads the current `emissionPerSecond` from `IStakeToken(STK_AAVE).assets(STK_AAVE)`, reads `currentAllowance = AAVE.allowance(EcosystemReserve, stkAAVE)`, and sets the new allowance to `currentAllowance + emissionPerSecond * 90 days` via two `AaveEcosystemReserveController.approve` calls (first to `0`, then to the target) routed through the Aave Ecosystem Reserve (`0x25F2226B597E8F9514B3F68F00f494cF4f286491`) on AAVE (`0x7Fc66500c84A76Ad7e9c93437bFc5Ac33E2DDaE9`) for spender stkAAVE (`0x4da27a545c0c5B758a6BA100e3a049001de870f5`).
* We have verified that the on-chain effect matches the formula: the seatbelt state-diff moves the allowance from `2,315,859,651,707,279` wei (`0.0023` AAVE) to `19,800,002,315,859,649,403,279` wei (`19,800.0023` AAVE), a delta of `19,799,999,999,999,997,696,000` wei. This is exactly `emissionPerSecond × 7,776,000 s` for `emissionPerSecond = 2,546,296,296,296,296` wei/s (≈ `0.002546` AAVE/s) — confirming the funding extension equals 90 days at the current, unchanged emission rate.
* We have verified the reset-to-0-then-set pattern via the two `Approval` events emitted by the AAVE token, with `owner = Ecosystem Reserve`, `spender = stkAAVE`, `value = 0` followed by `value = 19,800.0023 AAVE`.
* We have verified that no other state changes occur.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.