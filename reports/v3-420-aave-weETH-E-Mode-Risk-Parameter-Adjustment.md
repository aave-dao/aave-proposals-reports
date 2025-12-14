# Proposal 420. weETH E-Mode Risk Parameter Adjustment on Aave V3 Plasma Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=420)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/direct-to-aip-weeth-e-mode-risk-parameter-adjustment-on-aave-v3-plasma-instance/23381)

### Payloads

* Plasma - [proposal payloads](https://plasmascan.to/address/0x1e5739466aa331b5114C0570278A107864Ae91c6)



## Certora Analysis

### Proposal Types

* :wrench: :bar_chart: Configuration updates


### Context
The proposal recommends increasing the LT and LTV of Ether.fi restaked ETH in the weETH Stablecoin E-Mode on the Plasma instance in order to align the risk parameters of the asset in the E-Mode to the baseline configuration of weETH on the Ethereum Core instance.

### Proposal Creation
Transaction: [0xc97a71c4d59668b6fac0a0ba86328272b36028f4debd482bc905017b90368c3e](https://etherscan.io/tx/0xc97a71c4d59668b6fac0a0ba86328272b36028f4debd482bc905017b90368c3e)
- `proposalId`: 420
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x8959caf70649b5f854dea641758813e451dbf039da08cd0f0ae811a5cfaa6997

**`createProposal()` Parameters**
```
{
  "payloads": [ 
    { 
      "chain": "9745", 
      "accessLevel": "1", 
      "payloadsController": "0xe76EB348E65eF163d85ce282125FF5a7F5712A1d", 
      "payloadId": "11" 
    }, 
  ], 
  "votingPortal": "0x9Ded9406f088C10621BE628EEFf40c1DF396c172", 
  "ipfsHash": "0x8959caf70649b5f854dea641758813e451dbf039da08cd0f0ae811a5cfaa6997" 
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/11.md)

**Payload Reports**

* Plasma - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/11.md)


### Technical Analysis
We have verified consistency between the forum, IPFS, and the proposal’s payload. We have verified the integrity of the imports. We have checked the payload’s execution logic and validated it via Seatbelt. Verified EMode Category data.
The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.