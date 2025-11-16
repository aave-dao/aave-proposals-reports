# Proposal 408. XPL Onboarding

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=408)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-onboard-xpl-on-aave-v3-plasma-instance/23197)

### Payloads

* Plasma - [proposal payloads](https://plasmascan.to/address/0xb725a04BBa029b8150176Dd345c488bA13Ad1625)


## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context
This AIP proposes to onboard `XPL` to Aave V3 Plasma Instance.
This proposal will be a Direct to AIP. `XPL` is the native token of the Plasma blockchain. It was initially approved by governance for onboarding to the Plasma instance during the Plasma instance deployment yet was paused due to reservations of some service providers. Given there is now sufficient liquidity for the token we believe it is time to reconsider onboarding `XPL` to the Plasma instance.

### Proposal Creation
Transaction: [0xd01f72eb045ede7f91989e85fc1769f603f2f023c919c100af08216955c2e049](https://etherscan.io/tx/0xd01f72eb045ede7f91989e85fc1769f603f2f023c919c100af08216955c2e049)
- `proposalId`: 408
- `creator`: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xf17cd74c6709e5e976587a0db97b108b74e5a51a111220401143d57c64604a5f

**`createProposal()` Parameters**
```

```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/408.md)

**Payload Reports**

* Plasma - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/8.md)



### Technical Analysis

We have verified that the risk params match between the IPFS, payload and the forum. We have validate the seed supply amount. We have checked the correctness of the required addresses (`WXPL` and `ACI LM`). We have verified the creation of the E-Mode and its params.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.