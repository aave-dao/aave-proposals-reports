# Proposal 484. sGho Launch

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=484)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-sgho-launch-configuration/24346)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x4b2612332f8f73A445d79f7dAb34E246bF029061)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates

### Context
This publication provides an overview of the new native on-chain yield-accruing sGHO savings product upgrade. Within, we define the initial parameter configuration, present the migration process from the current sGHO (stkGHO rebranded), and introduce the new sGHO admin steward role.

The proposal sets a fixed Aave Savings Rate (ASR) of 4.25% APR (50 basis points above the Sky Savings Rate), refines the boost program from 8 boosts to 1 transitional boost, establishes the sGHO Steward as the rate governance mechanism, and defines an aggressive migration schedule from the legacy sGHO contract.

### Proposal Creation
Transaction: [0x0ef64597f44c31cac3c9cd765d07e17a47c5fff9dca52c1ae085f180d1f2221a](https://etherscan.io/tx/0x0ef64597f44c31cac3c9cd765d07e17a47c5fff9dca52c1ae085f180d1f2221a)
- `proposalId`: 484
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0xd128a32c304f7a258b12cb167a58723c773dd5cec003298e8a2393b3f2a7c037

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 435,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xd128a32c304f7a258b12cb167a58723c773dd5cec003298e8a2393b3f2a7c037",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/484.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/435.md)


### Technical Analysis

We have verified that the proposal launches the sGho savings module on Aave V3 Ethereum. Per the on-chain state-diff:

* sGho is deployed behind a proxy at `0xE1753F2e00940cC31213dd92013cF019DFE4ca1d`, with implementation `0xFF229A0bBb614a284De8aE0E41E5974878fD7c04`, an initial supply cap of `400,000,000` sGho, an initial exchange rate of `1e27` (1:1 with GHO in ray precision), and a target rate of `425` bps (4.25%).
* GHO (`0x40D16FC0246aD3160Ccc09B8D0D3A2cD28aE6C2f`) grants a `10,000,000` GHO facilitator bucket to `0x22740deBa78d5a0c24C58C740e3715ec29de1bFa`.
* On the sGho contract, the minter role is granted to `0x2CFe3ec4d5a6811f4B8067F0DE7e47DfA938Aa30`, the admin role is granted to the Aave Executor (`0x5300A1a15135EA4dc7aD5a167152C01EFc9b192A`), and the rate-update role is granted to the sGhoSteward (`0x60Bf2DF49F17529Cf956D57848ebEB8a0d0a2757`).
* The sGhoSteward additionally grants two operator roles to the Aave Executor.

We have verified that the payload does not list sGho as a reserve on any Aave V3 instance and does not perform any additional transfers.

We have verified the payload's logic and validated its execution via Seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.