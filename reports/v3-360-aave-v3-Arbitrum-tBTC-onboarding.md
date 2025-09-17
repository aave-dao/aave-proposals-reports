# Proposal 360. Onboard tBTC to Aave v3 on Arbitrum

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=360)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-onboard-tbtc-to-aave-v3-on-arbitrum/19756)

### Payloads

* Arbitrum One - [proposal payloads](https://arbiscan.io/address/0x33Af3ea7B0883C688ba3C395251140a12B28b5Bd)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets

### Context
This proposal seeks to onboard tBTC to Aave v3 on Arbitrum following a successful launch on Mainnet

### Proposal Creation
Transaction: [0x5ddf9c3a747d1408fb9e81390f9b9c99d034304cfd67c717f334d44672f08831](https://etherscan.io/tx/0x5ddf9c3a747d1408fb9e81390f9b9c99d034304cfd67c717f334d44672f08831)
- `proposalId`: 360
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x42534ee01faab1e4b069b31f48ec2ed9822f729d1ec5fe6fe5469f5f2b3cfc9f

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "42161",
            payloads_controller: "0x89644CA1bB8064760312AE4F03ea41b05dA3637C",
            payload_id: 100,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x42534ee01faab1e4b069b31f48ec2ed9822f729d1ec5fe6fe5469f5f2b3cfc9f",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/360.md)

**Payload Reports**

* Arbitrum One - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42161/0x89644CA1bB8064760312AE4F03ea41b05dA3637C/100.md)


### Technical Analysis
We have compared the risk parameters to the IPFS and forum and checked for correctness. We have validated the address of tBTC. We have checked the correctness of the supply of the tBTC seed with respect to decimal precision.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.