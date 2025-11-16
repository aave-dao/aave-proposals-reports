# Proposal 400. Addition of cbBTC/Stablecoin E-Mode to Aave V3 Base Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=400)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-addition-of-cbbtc-stablecoin-e-mode-to-aave-v3-base-instance/23174)

### Payloads

* Base - [proposal payloads](https://basescan.org/address/0x10c49f254B007144f6384db43555ea5d55A5dD49)



## Certora Analysis

### Proposal Types


* :wrench: :bar_chart: Configuration updates

### Context
Chaos Labs proposes introducing a tailored cbBTC Stablecoin E-Mode to the Base instance of Aave v3. Given the competitive cbBTC-collateral market and relatively low asset risk, combined with deep on-chain liquidity, the introduction of the E-Mode will increase the asset’s capital efficiency, making USDC and GHO borrowing more competitive.

### Proposal Creation
Transaction: [0xf901bb63161d81ecf9ad72f077b5b0f565178aa640e2800fd33f0c15d03c1936](https://etherscan.io/tx/0xf901bb63161d81ecf9ad72f077b5b0f565178aa640e2800fd33f0c15d03c1936)
- `proposalId`: 400
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x0a4a9e52e40bc22374361dee7b26ae2e5c33cf2abfe97492f80460146a74c1f8

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 89,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x0a4a9e52e40bc22374361dee7b26ae2e5c33cf2abfe97492f80460146a74c1f8",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/400.md)

**Payload Reports**

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/89.md)


### Technical Analysis
We have confirmed alignment between the forum post, the IPFS content, and the on-chain payload.
We have validated that the payload's logic is correct and will perform as intended.
We have checked the execution simulation via seatbelt

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.