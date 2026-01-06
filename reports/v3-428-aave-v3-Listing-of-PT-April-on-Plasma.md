# Proposal 428. Listing of PT Ethena April Maturity on Plasma Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=428)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-onboard-usde-susde-april-expiry-pt-tokens-on-aave-v3-plasma-instance/23515)

### Payloads

* Plasma - [proposal payloads](https://plasmascan.to/address/0x416Acb65Ba1C93A3D4c451efC913178Ce24da4Fe)



## Certora Analysis

### Proposal Types

* :handshake: Permission granting and revoking
* :wrench: :bar_chart: Configuration updates
* :gem: :new: Listing new assets


### Context
This AIP proposes to onboard USDe and sUSDe April expiry PT tokens on Aave V3 Plasma Instance.
* motivation - The previous USDe and sUSDe PT tokens that were onboarded have brought significant inflows to Aave, in preparation for the expiry and rollover we propose to onboard the next expiry of this PT token. We expect at a minimum that deposits will match those in the current expiry PT token, with potentially some sidelined demand.

### Proposal Creation
Transaction: [0xe9c1f7f4eb8a1954175548a9218931467faef0971be22975271a6aaab28ea64a](https://etherscan.io/tx/0xe9c1f7f4eb8a1954175548a9218931467faef0971be22975271a6aaab28ea64a)
- `proposalId`: 428
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x724572648ae49a362eaec129e0d0662c38986a3b32606201c582d6c37f4f0031

**`createProposal()` Parameters**
```
{
  "payloads": [ 
    { 
      "chain": "9745", 
      "accessLevel": "1", 
      "payloadsController": "0xe76EB348E65eF163d85ce282125FF5a7F5712A1d", 
      "payloadId": "13" 
    }, 
  ], 
  "votingPortal": "0x9Ded9406f088C10621BE628EEFf40c1DF396c172", 
  "ipfsHash": "0x724572648ae49a362eaec129e0d0662c38986a3b32606201c582d6c37f4f0031" 
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/13.md)

**Payload Reports**

* Plasma - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/13.md)


### Technical Analysis

We have confirmed alignment between the forum, IPFS, and the payload.
We have checked the integrity of the imports.
We have verified the `PT_sUSDE_9APR2026` and `PT_USDe_9APR2026` token addresses and their corresponding price feeds.
We have verified the `PT_sUSDE_9APR2026_LM_ADMIN` and `PT_USDe_9APR2026_LM_ADMIN` addresses.
We have validated the initial supply logic with respect to decimal precision.
We have checked E-Mode creation, assets, and parameters.
We have checked the new listing of the PT tokens and their risk parameters.




The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.