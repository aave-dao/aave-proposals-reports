# Proposal 399. USDC (old) deprecation on Gnosis Chain Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=399)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-usdc-old-deprecation-on-gnosis-chain-instance/23189)

### Payloads

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x166159E6ea11aC9feBBA7e7535acF4452c9741E2)



## Certora Analysis

### Proposal Types


* :wrench: :bar_chart: Configuration updates


### Context
This publication proposes the deprecation of the legacy USDC market on the Aave Gnosis Chain deployment. The deprecation will be executed by freezing the reserve (preventing new deposits, borrows, or collateral usage) and immediately increasing the Reserve Factor (RF) to 80%.

This aligns with the broader ecosystem effort to establish USDC.e (Circle-supported) as the canonical USDC representation on Gnosis Chain, consolidating liquidity and improving capital efficiency across Aave markets.

### Proposal Creation
Transaction: [0x0ecea0c744b272e5663b041d2aca92a012b2d3c96bdfc23e53cc8a863c9a9d12](https://etherscan.io/tx/0x0ecea0c744b272e5663b041d2aca92a012b2d3c96bdfc23e53cc8a863c9a9d12)
- `proposalId`: 399
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x9e06dab39bafb030dc63964e505beb4a258ee6f6373ecc43debb7681d7a54697

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "100",
            payloads_controller: "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
            payload_id: 65,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x9e06dab39bafb030dc63964e505beb4a258ee6f6373ecc43debb7681d7a54697",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/399.md)

**Payload Reports**

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/65.md)


### Technical Analysis

We have validate the alignment between the forum, IPFS and the on-chain payload.
We have verified `USDC_UNDERLYING` address. We checked that the RF,freeze changed as intended.
We confirmed payload's logic and checked its execution using seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.