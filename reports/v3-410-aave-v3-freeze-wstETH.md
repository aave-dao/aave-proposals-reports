# Proposal 410. Freeze wstETH Plasma

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=410)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-freeze-wsteth-on-plasma/23400)

### Payloads

* Plasma - [proposal payloads](https://plasmascan.to/address/0x4be4227A716144580e8B56f7c0db424172a4A89c)


## Certora Analysis

### Proposal Types

:wrench: :bar_chart: Configuration updates


### Context
Freeze wstETH on Plasma instance. 
Last week, Lido announced that Chainlink's CCIP will be the official cross-chain infrastructure for wstETH. While the wstETH representation on Plasma was already deployed through CCIP, it was unfortunately not set up in a fully future-proof manner.

Together with Chainlink, they have decided to redeploy the token contract to ensure the deployment is in line with the new cross-chain strategy. They ask us to deprecate the asset.

### Proposal Creation
Transaction: [0x926c4d3eb7547bbe0f39134d34a734ba0ff44540fbf6c3ed0621acb911e48984](https://etherscan.io/tx/0x926c4d3eb7547bbe0f39134d34a734ba0ff44540fbf6c3ed0621acb911e48984)
- `proposalId`: 410
- `creator`: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x5be17287148bec343b39d20f7ab0b8cf25ed1cd33a05b1545b4a963333c32c13

**`createProposal()` Parameters**
```
{
  "payloads": [ 
    { 
      "chain": "9745", 
      "accessLevel": "1", 
      "payloadsController": "0xe76EB348E65eF163d85ce282125FF5a7F5712A1d", 
      "payloadId": "9" 
    }, 
  ], 
  "votingPortal": "0x9Ded9406f088C10621BE628EEFf40c1DF396c172", 
  "ipfsHash": "0x5be17287148bec343b39d20f7ab0b8cf25ed1cd33a05b1545b4a963333c32c13" 
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/9.md)

**Payload Reports**

* Plasma - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/9.md)


### Technical Analysis

We have confirmed alignment between the forum post, the IPFS content, and the on-chain payload.
We have verified the relevant addresses and the amounts specified bith in the forum and IPFS.
We have validated payload's logic and reviewed seatbelt's execution.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.