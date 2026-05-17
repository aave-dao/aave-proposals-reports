# Proposal 476. Onboard USDe to the Aave V3 MegaETH Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=476)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-onboard-usde-to-the-aave-v3-megaeth-instance/24389)

### Payloads

* MegaETH - [proposal payloads](https://mega.etherscan.io/address/0x62dd7160f2cd88974e6c5047948cbf6db093ee43)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates
* :gem: :new: Listing new assets


### Context
This proposal seeks to onboard USDe to the Aave V3 MegaETH instance. The asset is already established across multiple Aave deployments, and on MegaETH it is expected to support stablecoin borrowing and yield-oriented usage with an initial onchain liquidity base already seeded for the market.

### Proposal Creation
Transaction: [0x2eaac132bc54c1030682f6d8c13aaa10ab13e234e53e936f818530a6946e8909](https://etherscan.io/tx/0x2eaac132bc54c1030682f6d8c13aaa10ab13e234e53e936f818530a6946e8909)
- `proposalId`: 476
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0x0588390064f99ff8b9440c7ea61a15e82a9118329ac1c9b47781ef9c335159ae

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "4326",
            payloads_controller: "0x80e11cB895a23C901a990239E5534054C66476B5",
            payload_id: 6,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x0588390064f99ff8b9440c7ea61a15e82a9118329ac1c9b47781ef9c335159ae",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/476.md)

**Payload Reports**

* MegaETH - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/4326/0x80e11cB895a23C901a990239E5534054C66476B5/6.md)


### Technical Analysis
We have verified the USDe token address `0x5d3a1Ff2b6BAb83b63cd9AD0787074081a52ef34`.  
We have verified the seed amount of 100 USDe (`100e18`) against the asset's 18-decimal precision.  
We have checked alignment of the general reserve parameters between forum, IPFS and payload.
We have verified the LM admin address `0xac140648435d03f784879cd789130F22Ef588Fcd` is applied to the underlying, aToken, and vToken via the EmissionManager.  
We have checked the USDe-Stablecoins e-mode parameters.  
We have checked the payload's logic and verified its execution via the seatbelt

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.