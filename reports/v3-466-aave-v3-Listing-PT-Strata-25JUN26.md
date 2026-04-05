# Proposal 466. Listing PT Strata 25JUN2026

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=466)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-onboard-strata-srusde-june-expiry-pt-tokens-to-v3-core-instance/24313)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0xeE1E71E981f160524aA136a06Fbf2893435E010B)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates
* :gem: :new: Listing new assets


### Context
This proposal seeks to onboard Strata srUSDe June PT tokens to the Aave V3 Core Instance.

### Proposal Creation
Transaction: [0x84dfbd696bad0639e2b9e1b7392f1bd347227d08afb1495ed21e013956f24806](https://etherscan.io/tx/0x84dfbd696bad0639e2b9e1b7392f1bd347227d08afb1495ed21e013956f24806)
- `proposalId`: 466
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x7b179fadb321542f8bde096eed9fafe9667d924e141f8d705a242e94658a1475

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 422,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x7b179fadb321542f8bde096eed9fafe9667d924e141f8d705a242e94658a1475",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/466.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/422.md)


### Technical Analysis
We have confirmed the new listing of `PT_srUSDe_25JUN2026` with the correct parameters, and verified the seed amount with respect to decimal precision.

We have verified that id = 0 maps to `EModeCategoryUpdate` and id = 1 maps to `PendleDiscountRateUpdate`.

Additionally, `0xac140648435d03f784879cd789130F22Ef588Fcd` is set as the emission admin for the token and the corresponding aToken and vToken.

We have confirmed the pre-execution logic returning the 100 inadvertently transferred `PT-srUSDe-2APR2026` tokens back to the Strata seeding address.

We have checked the price feed for the newly listed token.

We have verified the creation of the two new E-modes (Stablecoins and USDe) with the correct risk parameters.

We have verified proposal logic and validate its execution via seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.