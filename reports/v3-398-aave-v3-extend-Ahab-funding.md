# Proposal 398. Extend Ahab Funding

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=398)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-extend-ahab-funding/23213/2)

### Payloads

* Ethereum - [proposal payloads](https://etherscan.io/address/0x2EC96449AC88CD32dee578A7FE0f600fBdf9BfD5)

* Plasma - [proposal payloads](https://plasmascan.to/address/0xDc419E7FCae1EaAcEbb0da69f9d88FD3Aa41DDac)


## Certora Analysis

### Proposal Types

* :moneybag: :receipt: Asset transfers
* :handshake: Permission granting and revoking


### Context
In collaboration with Aave’s Growth teams, this proposal introduces a flexible funding mechanism to support incentive commitments made by Service Providers in the establishment of strategic partnerships.

### Proposal Creation
Transaction: [0x8b561ff69154eb95b4a0675becad9fb89aadcecfb5cd860f078c9f79f9354a9a](https://etherscan.io/tx/0x8b561ff69154eb95b4a0675becad9fb89aadcecfb5cd860f078c9f79f9354a9a)
- `proposalId`: 398
- `creator`: 0x57ab7ee15ce5ecacb1ab84ee42d5a9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xa0d31fce6efc2bc02c5704ad753a2aca4d085858189d73228f2cb783da9afe41

**`createProposal()` Parameters**
```
{
  "payloads": [ 
    { 
      "chain": "1", 
      "accessLevel": "1", 
      "payloadsController": "0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5", 
      "payloadId": "363" 
    }, 
    { 
      "chain": "9745", 
      "accessLevel": "1", 
      "payloadsController": "0xe76EB348E65eF163d85ce282125FF5a7F5712A1d", 
      "payloadId": "7" 
    }, 
  ], 
  "votingPortal": "0x9Ded9406f088C10621BE628EEFf40c1DF396c172", 
  "ipfsHash": "0xa0d31fce6efc2bc02c5704ad753a2aca4d085858189d73228f2cb783da9afe41" 
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/398.md)

**Payload Reports**

* Ethereum - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/1/0xdAbad81aF85554E9ae636395611C58F7eC1aAEc5/363.md)

* Plasma - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/9745/0xe76EB348E65eF163d85ce282125FF5a7F5712A1d/7.md)

### Technical Analysis

We have confirmed alignment between the forum post, the IPFS content, and the on-chain payload.
We have verified `aEthWETH`, `aEthGHO` and `aEthUSDS` assets addresses on Ethereum,
`aPlaUSDT0`, `aPlaUSDe` on plasma. Also `Ahab` as spender on Ethereum and Plasma, `AFC SAFE` as spender on Ethereum and the amounts. We have reviewed payload's logic and checked the execution via seatbelt. 

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.