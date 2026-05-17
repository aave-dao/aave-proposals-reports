# Proposal 472. Onboard PT-USDG 28MAY2026 on V3 Core

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=472)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-onboard-pt-usdg-28may2026-to-aave-v3-core-instance/24345/4)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x1BBE770bDf9125c218EaBDCdf0252264A226Acdc)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates
* :gem: :new: Listing new assets


### Context
This AIP proposes to onboard PT-USDG-28MAY2026 to the Aave V3 Core Instance on Ethereum.

### Proposal Creation
Transaction: [0xe9ad0a09219b32df56541ecf6791b0bae4c5c6994a7c41da6b2b8e746a63ebd1](https://etherscan.io/tx/0xe9ad0a09219b32df56541ecf6791b0bae4c5c6994a7c41da6b2b8e746a63ebd1)
- `proposalId`: 472
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0xa8e20e98a656582b6fe588cb99bc3e72fe76bc8810407b7d7ad14fbd2003cffd

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "1",
            payloads_controller: "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5",
            payload_id: 427,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0xa8e20e98a656582b6fe588cb99bc3e72fe76bc8810407b7d7ad14fbd2003cffd",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/472.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/427.md)


### Technical Analysis
We have verified the PT-USDG-28MAY2026 token address `0x9db38D74a0D29380899aD354121DfB521aDb0548`.  
We have verified the seed amount of 100 PT-USDG (`100e6`) against the asset's 6-decimal precision.  
We have checked alignment of the general reserve parameters between forum, IPFS and payload.  
We have verified the LM admin address `0xac140648435d03f784879cd789130F22Ef588Fcd` is applied to the underlying, aToken, and vToken via the EmissionManager.
We have checked the PT_USDG_28MAY2026__Stablecoins e-mode parameters.
We have checked the payload's logic and verified its execution via the seatbelt.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.