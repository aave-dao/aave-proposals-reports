# Proposal 317.  Onboarding wETH to Aave V3 Celo Instance

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=317)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-onboarding-weth-to-aave-v3-celo-instance/21750)

### Payloads

* Celo - [proposal payloads](https://celo.blockscout.com/address/0xbC92267704FD76Cb14769020499965C264120f2E)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context
This AIP proposes the onboarding of Wrapped Ether (wETH) as a supported asset on the Aave V3 Celo Instance. The integration aims to expand the protocol’s utility and provide users with additional opportunities for lending and borrowing.

### Proposal Creation
Transaction: [0x318bdd93e50d6e092a704848cc880ed99d94cdd687a78190350c3247646a287e](https://etherscan.io/tx/0x318bdd93e50d6e092a704848cc880ed99d94cdd687a78190350c3247646a287e)
- `proposalId`: 317
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0xa8dccd16ebf9dd7ba9d427b27b58961efeeab04d0f3bdcb61a4ff1d33a1b6c56

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "42220",
            payloads_controller: "0xE48E10834C04E394A04BF22a565D063D40b9FA42",
            payload_id: 4,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0xa8dccd16ebf9dd7ba9d427b27b58961efeeab04d0f3bdcb61a4ff1d33a1b6c56",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/317.md)

**Payload Reports**

* Celo - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/42220/0xE48E10834C04E394A04BF22a565D063D40b9FA42/4.md)


### Technical Analysis
We have verified the seed amount that was supplied is enough and in the correct precision, additionally we have confirmed the risk parameters are configured as intended.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.