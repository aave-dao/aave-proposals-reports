# Proposal 447. Increase WBTC Liquidation Bonus and EURS Reserve Factor on Polygon V3

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=447)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-increase-wbtc-liquidation-bonus-and-eurs-reserve-factor-on-polygon-v3/24029)

### Payloads

* Polygon - [proposal payloads](https://polygonscan.com/address/0x49c234368bb90c3Fe4E55Bd1A3b50c391DCfA505)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
This proposal recommends (i) increasing the liquidation bonus (LB) for WBTC on Aave v3 Polygon from 7% to 8.5%, and (ii) increasing the EURS reserve factor from 50% to 99%.

### Proposal Creation
Transaction: [0xb4ef9ba9ce0cd488ca2550de73f48f0fe855105f2080379c33dcc09b9dad610f](https://etherscan.io/tx/0xb4ef9ba9ce0cd488ca2550de73f48f0fe855105f2080379c33dcc09b9dad610f)
- `proposalId`: 447
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x8d8863fe9c4e386608530c08edb6cb0a3a5988d0479354597f1fdd45bfb150cb

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "137",
            payloads_controller: "0x401B5D0294E23637c18fcc38b1Bca814CDa2637C",
            payload_id: 138,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x8d8863fe9c4e386608530c08edb6cb0a3a5988d0479354597f1fdd45bfb150cb",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/447.md)

**Payload Reports**

* Polygon - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/137/0x401B5D0294E23637c18fcc38b1Bca814CDa2637C/138.md)


### Technical Analysis

We have validated the parameter updates for both `WBTC` and `EURS`.
We have reviewed the payload logic and verified its execution using Seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.