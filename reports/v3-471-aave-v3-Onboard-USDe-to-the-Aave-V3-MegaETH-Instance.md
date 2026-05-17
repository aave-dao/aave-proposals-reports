# Proposal 471. Onboard USDe to the Aave V3 MegaETH Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=471)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-onboard-usde-to-the-aave-v3-megaeth-instance/24389)

### Payloads

* MegaETH - [proposal payloads](https://mega.etherscan.io/address/0x892361c1977041fc1a4cac04dd2a653384878200)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates
* :gem: :new: Listing new assets

## Context
```
Greetings Aave community,

The MegaETH proposal, proposal 471, that was expected to execute yesterday was delayed on the voting chain, Avalanche, during the switch from the Chainlink API-based execution flow to CRE. This delay prevented the Aave Robot from automatically executing the proposal’s payload.

BGD handled the Chainlink CRE transition and assisted in resolving the voting delay. Today, after Proposal 473 passed, BGD manually executed the payload, upgrading the MegaETH deployment from Aave V3.6 to Aave V3.7.

The protocol is functioning as intended. Proposal 471 was built against the previous V3.6 deployment, and is no longer valid for execution in its current form. This proposal must expire and be re-proposed to the current V3.7 deployment.

Aave Labs
```
### Proposal Creation
Transaction: [0x5d64cd57c659fa5d6edac0904c021452e9d762300cf5d60cb671f5104d3926e1](https://etherscan.io/tx/0x5d64cd57c659fa5d6edac0904c021452e9d762300cf5d60cb671f5104d3926e1)
- `proposalId`: 471
- `creator`: 0x66a28531E6f390A8CD44aB0C57a0F1aeb7E673FF
- `accessLevel`: 1
- `ipfsHash`: 0x9cb8ea1270bc549b397bb2e95afbe43d1c2c55f52cd026150966e303244959d3

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "4326",
            payloads_controller: "0x80e11cB895a23C901a990239E5534054C66476B5",
            payload_id: 5,
        },
    ],
    voting_portal: "0x9Ded9406f088C10621BE628EEFf40c1DF396c172",
    ipfs_hash: "0x9cb8ea1270bc549b397bb2e95afbe43d1c2c55f52cd026150966e303244959d3",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/471.md)

**Payload Reports**

* MegaETH - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/4326/0x80e11cB895a23C901a990239E5534054C66476B5/5.md)


### Technical Analysis

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.