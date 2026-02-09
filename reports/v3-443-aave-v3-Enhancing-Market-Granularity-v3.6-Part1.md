# Proposal 443. Enhancing Market Granularity in Aave v3.6: Part 1

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=443)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-enhancing-market-granularity-in-aave-v3-6-restricting-borrowability-and-collateralization-outside-of-liquid-emodes/23592)

### Payloads

* OP Mainnet - [proposal payloads](https://optimistic.etherscan.io/address/0x302a5A9dB26b70c57A0DFe7B0e68DB8Ff53d0BF6)

* Metis - [proposal payloads](https://explorer.metis.io/address/0xF2A98958083B9cd0C385dACD0BfAB08BF747D7Cf)

* Gnosis - [proposal payloads](https://gnosisscan.io/address/0x2CEdBD9B9EB4A2096bA355DCDF9582e923CBFfBB)

* Scroll - [proposal payloads](https://scrollscan.com/address/0xeAe5c9e22D7f545929Cc19a89eD0414304527D89)

* Celo - [proposal payloads](https://celo.blockscout.com/address/0xB165213234EC7a00dA29B17bD1230907c21C602b)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
This proposal leverages the configurability improvements introduced in Aave v3.6 to strengthen risk isolation and improve parameter clarity. Specifically, it introduces:

LTV0 for assets not intended to serve as collateral outside of eModes.
Non-borrowable status for assets whose use cases are restricted to within their respective eModes.
Exclusive eMode participation, ensuring these assets are only active within targeted, high-correlation environments.
This aims to reduce systemic exposure, simplify risk management, and enable cleaner differentiation between general market assets and those intended for correlated or high-efficiency lending environments.

### Proposal Creation
Transaction: [0x5205321a96ad81029456ceb5c891c7efca2d5a5dc28b4da3afd1bf03f7dfe71c](https://etherscan.io/tx/0x5205321a96ad81029456ceb5c891c7efca2d5a5dc28b4da3afd1bf03f7dfe71c)
- `proposalId`: 443
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x5fd9bc11bc15c390ad9873ef69dcdd4e329fb1f77b9b08db8464230f15a73aa8

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "10",
            payloads_controller: "0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4",
            payload_id: 92,
        },
        {
            chain: "1088",
            payloads_controller: "0x2233F8A66A728FBa6E1dC95570B25360D07D5524",
            payload_id: 46,
        },
        {
            chain: "100",
            payloads_controller: "0x9A1F491B86D09fC1484b5fab10041B189B60756b",
            payload_id: 71,
        },
        {
            chain: "534352",
            payloads_controller: "0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE",
            payload_id: 49,
        },
        {
            chain: "42220",
            payloads_controller: "0xE48E10834C04E394A04BF22a565D063D40b9FA42",
            payload_id: 10,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x5fd9bc11bc15c390ad9873ef69dcdd4e329fb1f77b9b08db8464230f15a73aa8",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/443.md)

**Payload Reports**

* OP Mainnet - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/10/0x0E1a3Af1f9cC76A62eD31eDedca291E63632e7c4/92.md)

* Metis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1088/0x2233F8A66A728FBa6E1dC95570B25360D07D5524/46.md)

* Gnosis - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/100/0x9A1F491B86D09fC1484b5fab10041B189B60756b/71.md)

* Scroll - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/534352/0x6b6B41c0f8C223715f712BE83ceC3c37bbfDC3fE/49.md)

* Celo - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42220/0xE48E10834C04E394A04BF22a565D063D40b9FA42/10.md)


### Technical Analysis

We checked alignment between the governance forum IPFS link and the payload.  
We verified that the correct collateral updates and borrow disablements were applied to the intended assets on the intended chains.  
We validated the payload logic and behavior, and verified execution via Seatbelt.  
The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.