# Proposal 474. GHO Inclusion into E-Modes on Aave V3 Plasma

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=474)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-change-of-supply-caps-and-adjustment-of-e-mode-assets-on-aave-v3-07-04-26/24396)

### Payloads

* Plasma - [proposal payloads](https://plasmascan.to/address/0x9c66833dd17fbd99413839c041f265d01ac6ea36)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
Chaos Labs proposed the following change to be implemented through AIP:

Include GHO within the PT asset E-modes on the Plasma Instance
The supply cap increases included in this proposal (PT-sUSDe-18JUN2026 on Plasma, PT-srUSDe-25JUN2026 on Ethereum Core, wrsETH and FBTC on Mantle) will be executed via Risk Stewards and are not part of this AIP.

### Proposal Creation
Transaction: [0x22d0981fd0bd69f3426ea446901a590c3c61f66992ce97b3061cd308553d3a79](https://etherscan.io/tx/0x22d0981fd0bd69f3426ea446901a590c3c61f66992ce97b3061cd308553d3a79)
- `proposalId`: 474
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xee9efdbd8b477dade0fc71f4285558f64628c0f38943c2dfd21462a59e37f993

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "9745",
            payloads_controller: "0xe76EB348E65eF163d85ce282125FF5a7F5712A1d",
            payload_id: 23,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xee9efdbd8b477dade0fc71f4285558f64628c0f38943c2dfd21462a59e37f993",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/474.md)

**Payload Reports**

* Plasma - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/23.md)


### Technical Analysis
* We have verified the E-Mode category label updates and asset assignments, ensuring GHO is correctly enabled for borrowing within the specified categories without altering existing risk parameters.

* We have verified the payload logic and validate its execution via seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.