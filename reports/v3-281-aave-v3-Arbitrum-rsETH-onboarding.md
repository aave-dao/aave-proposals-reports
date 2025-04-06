# Proposal 281.  Onboard rsETH to Arbitrum

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=281)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-onboard-rseth-to-arbitrum-and-base-v3-instances/20741)

### Payloads

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0x4E3FC84748541ED0d20dFA41f5E5c38bB0D66Cfe)


## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context
Onboard rsETH to the Aave V3 Arbitrum.

### Proposal Creation
Transaction: [0xe832e8029f3d0a78886e829f02944b94c4e042f0a47b3a91da05cdfa7075e68d](https://etherscan.io/tx/0xe832e8029f3d0a78886e829f02944b94c4e042f0a47b3a91da05cdfa7075e68d)
- `proposalId`: 281
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x7824ef23dfa3dafbc74744a92d482ba61a72ebeec7a941a70134d63809755a92

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 82,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x7824ef23dfa3dafbc74744a92d482ba61a72ebeec7a941a70134d63809755a92",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/281.md)

**Payload Reports**

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/82.md)


### Technical Analysis
We have compared the risk parameters, made sure enough rsETH was supplied to the pool.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.