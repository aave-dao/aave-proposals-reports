# Proposal 314. Onboard eUSDe and eUSDe based PT token to Aave V3 Core

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=314)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-onboard-usde-july-expiry-pt-tokens-on-aave-v3-core-instance/22041)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xa84a25756B59C4bB19CC20cCBD0747816e37C5B0)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context
This proposal aims to onboard the eUSDe token as well as the USDe July expiry PT tokens and eUSDe August expiry PT tokens on the Aave V3 Core Instance.

### Proposal Creation
Transaction: [0xb2dffd3c14be43a0863214ea8d6287fd10dfb167c4f95ce75dcdcecf6a09e971](https://etherscan.io/tx/0xb2dffd3c14be43a0863214ea8d6287fd10dfb167c4f95ce75dcdcecf6a09e971)
- `proposalId`: 314
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xa82674c1b37d426e52051d98954abd7791774c807524ecd7959b8a0c89ea6a5b

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 290,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xa82674c1b37d426e52051d98954abd7791774c807524ecd7959b8a0c89ea6a5b",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/314.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/290.md)


### Technical Analysis
We conducted a side-by-side verification of all configured risk parameters for eUSDe, PT_USDe_31JUL2025, and PT_eUSDe_14AUG2025 against the on-chain payload. Every percentage parameter (LTV, liquidation threshold, liquidation bonus, reserve factor, rate slopes, protocol fees) was correctly scaled (×10 000) and matches the IPFS specification. Debt ceilings remain at zero, consistent with isolation mode being disabled, and flashloan, borrowable, and collateral flags align precisely with the intended settings.

The newly introduced E-mode categories (IDs 10–15 (not including 11)) were added without modifying any pre-existing categories. Each category’s LTV, liquidation threshold, and bonus correspond exactly to the proposed values, ensuring backward compatibility. Asset-level E-mode assignments for PT and underlying stablecoins were also validated, except for one mismatched flag in the PT-USDe July-2025 table, which we have flagged for correction.

Finally, all price‐feed addresses in the new listings payload match the on‐chain oracles referenced in the proposal, and no feed parameters (discount rates, snapshot windows) were altered. This confirms that market data inputs remain accurate and unchanged.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.