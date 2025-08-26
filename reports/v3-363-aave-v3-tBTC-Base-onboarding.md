# Proposal 363. Onboard tBTC to Aave v3 on Base

### Voting Link
[Link to voting page](https://vote.onaave.com/proposal/?proposalId=363)

### Governance Forum Discussion
[Link to forum discussion](https://governance.aave.com/t/arfc-onboard-tbtc-to-aave-v3-on-base/22226)

### Payloads

* Base - [proposal payloads](https://basescan.org/address/0xfb30cc9E3bd7409d0C3bdfeB23cC71Ad9AAe6fd1)



## Certora Analysis

### Proposal Types

* :gem: :new: Listing new assets


### Context
This proposal seeks to onboard tBTC to Aave v3 on Base.

### Proposal Creation
Transaction: [0x2b2e8fa47d2f8080805cc4196ccb43759274f448623cd9f3688b531703c6d038](https://etherscan.io/tx/0x2b2e8fa47d2f8080805cc4196ccb43759274f448623cd9f3688b531703c6d038)
- `proposalId`: 363
- `creator`: 0x57ab7ee15cE5ECacB1aB84EE42D5A9d0d8112922
- `accessLevel`: 1
- `ipfsHash`: 0x2a7103c2000298745175ca820ca7c0e7b7c162d2ed8df0c1858b924134b78be4

**`createProposal()` Parameters**
```
{
    payloads: [
        {
            chain: "8453",
            payloads_controller: "0x2DC219E716793fb4b21548C0f009Ba3Af753ab01",
            payload_id: 85,
        },
    ],
    voting_portal: "0xFe4683C18aaad791B6AFDF0a8e1Ed5C6e2c9ecD6",
    ipfs_hash: "0x2a7103c2000298745175ca820ca7c0e7b7c162d2ed8df0c1858b924134b78be4",
    access_level: 1,
}
```

### Aave Seatbelt Report
**Proposal Report**

[Link to Seatbelt proposal report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/proposals/363.md)

**Payload Reports**

* Base - [payload Seatbelt report](https://github.com/bgd-labs/seatbelt-gov-v3/blob/main/reports/payloads/8453/0x2DC219E716793fb4b21548C0f009Ba3Af753ab01/85.md)


### Technical Analysis
We have compared the risk parameters to forum and IPFS for inconsistencies. We have validated the seed amount. We have checked the price feed is correct.

The proposal is consistent with the description on both Snapshot and the governance forum.

### Certora validations
* :white_check_mark: The code on the proposal payload corresponds to the proposal specification.
* :white_check_mark: The proposal includes a proper tests suite, checking all necessary post-conditions.
* :white_check_mark: BGD reviewed the payload before the proposal was submitted.
* :white_check_mark: Certora reviewed the procedure followed to submit the proposal.