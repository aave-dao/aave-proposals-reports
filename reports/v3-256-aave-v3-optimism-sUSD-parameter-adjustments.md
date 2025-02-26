# Proposal 256. sUSD Risk Parameter Adjustment

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=256)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-susd-risk-parameter-adjustment/20793)

### Payloads

* OP Mainnet - [proposal payloads](https://optimistic.etherscan.io/address/0x5BF166C82849d2d12F3bC7116add22B81D689CeC)



## Certora Analysis

### Proposal Types
* :wrench: :bar_chart: Configuration updates

### Context
Following latest DEX liquidity, investment profile in the market and a relatively recent depeg event of sUSD, an adjustment of the colatteral parameters related to the token are proposed to be adjusted.

### Proposal Creation
Transaction: [0x3ac467bfd547845a7928eb59665afab496a2cdff2d5e62ad7c727e247463cede](https://etherscan.io/tx/0x3ac467bfd547845a7928eb59665afab496a2cdff2d5e62ad7c727e247463cede)
- `proposalId`: 256
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x723936aac15685cf6a4cb44f4252592631f5f0022953896cc51b57df418da6f7

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "10",
            payloads_controller: "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
            payload_id: 67,
        },
    ],
    voting_portal: "0x9b24C168d6A76b5459B1d47071a54962a4df36c3",
    ipfs_hash: "0x723936aac15685cf6a4cb44f4252592631f5f0022953896cc51b57df418da6f7",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/256.md)

**Payload Reports**

* OP Mainnet - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/67.md)


### Technical Analysis
The proposal was verified to update sUSD's LTV on Optimism to 0 to prevent further borrowing against it.
In addition, the stablecoin emode was also adjusted to effectively prevent further borrowing (LTV 0.01%) and small reduction in LT to 87%.
No other changes were made in this proposal for any other assets or on any other chains.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.